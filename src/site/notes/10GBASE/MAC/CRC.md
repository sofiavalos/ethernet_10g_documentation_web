---
{"dg-publish":true,"permalink":"/10-gbase/mac/crc/"}
---

A **cyclic redundancy check** (**CRC**) is an [error-detecting code](https://en.wikipedia.org/wiki/Error_correcting_code "Error correcting code") commonly used in digital [networks](https://en.wikipedia.org/wiki/Telecommunications_network "Telecommunications network") and storage devices to detect accidental changes to digital data.[1](https://en.wikipedia.org/wiki/Cyclic_redundancy_check#cite_note-Pundir_Sandhu_2021_p._103084-1)[2](https://en.wikipedia.org/wiki/Cyclic_redundancy_check#cite_note-Schiller_Mattes_2007_pp._944%E2%80%93949-2) Blocks of data entering these systems get a short _check value_ attached, based on the remainder of a [polynomial division](https://en.wikipedia.org/wiki/Polynomial_long_division "Polynomial long division") of their contents. On retrieval, the calculation is repeated and, in the event the check values do not match, corrective action can be taken against data corruption. CRCs can be used for [error correction](https://en.wikipedia.org/wiki/Error_detection_and_correction "Error detection and correction") (see [bitfilters](https://en.wikipedia.org/wiki/Mathematics_of_cyclic_redundancy_checks#Bitfilters "Mathematics of cyclic redundancy checks"))

To compute an _n_-bit binary CRC, line the bits representing the input in a row, and position the (_n_ + 1)-bit pattern representing the CRC's divisor (called a "[polynomial](https://en.wikipedia.org/wiki/Polynomial "Polynomial")") underneath the left end of the row.

In this example, we shall encode 14 bits of message with a 3-bit CRC, with a polynomial _x_3 + _x_ + 1. The polynomial is written in binary as the coefficients; a 3rd-degree polynomial has 4 coefficients (1_x_3 + 0_x_2 + 1_x_ + 1). In this case, the coefficients are 1, 0, 1 and 1. The result of the calculation is 3 bits long, which is why it is called a 3-bit CRC. However, you need 4 bits to explicitly state the polynomial.

Start with the message to be encoded:
```
11010011101100
```
This is first padded with zeros corresponding to the bit length _n_ of the CRC. This is done so that the resulting code word is in [systematic](https://en.wikipedia.org/wiki/Systematic_code "Systematic code") form. Here is the first calculation for computing a 3-bit CRC:

```
11010011101100 000 <--- input right padded by 3 bits
1011               <--- divisor (4 bits) = x³ + x + 1
------------------
01100011101100 000 <--- result
```
The algorithm acts on the bits directly above the divisor in each step. The result for that iteration is the bitwise XOR of the polynomial divisor with the bits above it. The bits not above the divisor are simply copied directly below for that step. The divisor is then shifted right to align with the highest remaining 1 bit in the input, and the process is repeated until the divisor reaches the right-hand end of the input row. Here is the entire calculation:

```
11010011101100 000 <--- input right padded by 3 bits
1011               <--- divisor
01100011101100 000 <--- result (note the first four bits are the XOR with the divisor beneath, the rest of the bits are unchanged)
 1011              <--- divisor ...
00111011101100 000
  1011
00010111101100 000
   1011
00000001101100 000 <--- note that the divisor moves over to align with the next 1 in the dividend (since quotient for that step was zero)
       1011             (in other words, it doesn't necessarily move one bit per iteration)
00000000110100 000
        1011
00000000011000 000
         1011
00000000001110 000
          1011
00000000000101 000
           101 1
-----------------
00000000000000 100 <--- remainder (3 bits).  Division algorithm stops here as dividend is equal to zero.
```

Since the leftmost divisor bit zeroed every input bit it touched, when this process ends the only bits in the input row that can be nonzero are the n bits at the right-hand end of the row. These _n_ bits are the remainder of the division step, and will also be the value of the CRC function (unless the chosen CRC specification calls for some postprocessing).

The validity of a received message can easily be verified by performing the above calculation again, this time with the check value added instead of zeroes. The remainder should equal zero if there are no detectable errors.

```
11010011101100 100 <--- input with check value
1011               <--- divisor
01100011101100 100 <--- result
 1011              <--- divisor ...
00111011101100 100

......

00000000001110 100
          1011
00000000000101 100
           101 1
------------------
00000000000000 000 <--- remainder
```