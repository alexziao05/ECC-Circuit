Circuit 1/Part 1.cct:
The use for circuit one in this lab would be to calculate parity bits depending on what the input of the data bits are. This is done through XORing the data of the data bits to be able to simulate whether there are an even or odd amount of ones for the parity bit to fix. The parity bits are going off of an even structure in this lab where if there is an even amount of 1’s it is 0 but if there is an odd amount of 1’s it will be 1. There is also a 5th parity bit that needs to be made through XORing both the data and parity bits. 




Circuit 2/Part 2.cct: 
The use for this circuit in the lab would be to introduce errors into the 13 bit bus. 
We do this by adding E1 through E13 to the inputs which correspond to the D1-D13 bits and we can make the binary switches of the E value 0 to not change the
D bit at all, and 1 to be able to switch the D value. The output being the D' series
shows the changed or unchanged D bits depending on whether or not the E bits were 0 or 1.


E = 1 means corresponding D bit is flipped
E = 0 means corresponding D bit is not flipped at all




Circuit 3/Part 3.cct:
The use for this circuit in the lab would be to determine errors that your new data has based off of the E values. If there is no error at all, then there would be a 0 displayed. If there is 1 error, then there would be a C displayed and if there are two errors, then an E would be displayed. This circuit also implements error correcting if there is only one error. The circuit makes use of the Part1, Part2, and Part 3 device symbols in order to calculate errors


Helper Part.cct:
This is a Part that’s used within Circuit #3. It basically takes in 12 data bit inputs and the parity bit, and carries out a XOR of the bits that are explained in Lecture 10 Slide 22, to calculate the 4 check bits. Once the 4 check bits are calculated, they are hooked up to Port Out’s. At the very bottom is a XOR of all of the data bits (including the parity bit). The syndrome is formed outside of the helper part.


2-to-4 Line Decoder/2-4 Decoder.cct:
This part is essentially a 2 Input, and 4 Output decoder. We couldn’t get the results that we wanted with LogicWork’s built-in 4-output Decoder that had an Enable input, so we made our own. However, even with making our own decoder part, we weren’t getting the outputs that we needed, so I changed all of the internal AND gates to AND gates with inverts, then I changed one of the gates to be an OR gate, then I added another OR gate. 


If this sounds like we didn’t know what we were doing, you’d be mostly wrong. We knew that the output had to match the Binary for the Hex letter’s ‘C’ and ‘E’ for the proper inputs, but we were only getting a 1 signal out of a single gate under any circumstance, unless we constructed the decoder like the way it currently is.


This setup gives us the EXACT outputs needed. Like, without fail, and under all tested inputs, whenever there is No Error, the Decoder outputs a 0. Whenever there is a Single-Bit error, the Decoder outputs a C to the Hex Display, and whenever there is a Multi-bit error, the Decoder outputs an E to the Hex Display. 


It works. And we understand its purpose, what it needs to do, and how it’s doing it. The process of creating the internal logic is the only part unclear to us. 






Contributions:
Alex Huang:  
Making of structure for circuits and implementation of circuits




Mateen Rahbar:
Research, making device symbols, and implementation of circuits. Specifically helped double check Part 1 and 2, and worked on the Part 3 part object within the Overall Part 3 schematic. 


David Soriano:
Making device symbols and implementation of circuits.