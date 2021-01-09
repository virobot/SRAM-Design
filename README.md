# SRAM-Design
This repository displays pictorial representation of a 512-bit SRAM Design. The SRAM design is completed with four 128-bit banks. The schematic and the layout are constructed with the help of Cadence Virtuoso. 

This project has been aimed for detailed understanding of SRAM memory READ and WRITE operations and have been successfully tested for its functionality. 

## Explanation for the Design of SRAM Memory Operation

* SRAM is a static random-access memory which consists of two cross-coupled inverters. There are two stable states, “0” and “1”. For a specific cell, the value to be written is stored in the cross coupled inverters.

* A SRAM cell is selected with the help of the word line. With this, we can create an array of the SRAM cell which is called as a bank. The access to each cell in the bank is made possible using the Row Decoder. The row decoder selected the exact row (word line) to access and thus helps with the functionality of reading and writing.

* During the write operation, the word line of the specified SRAM cell is raised and the value to be written (0 or 1) is provided through the bit lines. Thus, the value would then be stored in the cross-coupled inverters.

* During the read operation, the word line is raised again, and the sense amplifier assists with the reading circuitry. Its role is to help sense the low power signals and raise the voltage swing to recognizable logic levels so that the data can be interpreted properly by the logic outside the memory.

* In order to save space, we have used read and write mux. The read mux helps to select a 16 bit and bit bar lines which would then be passed through the sense amplifier to read the values. Rather than having 64 sense amplifiers, we reduce the number of sense amplifier to 16 with the help of read circuitry.

* For the write circuitry, we are saving space by reducing the write drives from 64 to just 16. Thus, the read and write multiplexers assists with the task of logic analysis and saving space.

* The use of the column mux (or bank select) in this case, helps with selecting the desired bit lines for reading and writing to the appropriate SRAM cell.

* Finally, the output is displayed through the flip-flop.

* Here the results have been verified by performing the READ and WRITE operation in a series of test events. 

* The design has undergone DRC as well as LVS check. 
