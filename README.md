# MIDI-recorder-and-player-on-STK500

Design and implementation of a MIDI recorder and player on Atmel STK500 with ATmega644

Overview

This project aims to design and implement a MIDI recorder and player using an Atmel STK500 board with an ATmega644 microcontroller. Devices attached to the STK500 include a MIDI keyboard via USART, SD card via SPI, a speaker and a LCD screen. A FAT32 system was developed to read or write data from or to SD card. Using these devices with the program developed from this project, users are able to record the MIDI tracks in SD card by playing the keyboard. The MIDI track then can be played on the device. In addition, MIDI tracks from other source (e.g. Internet) can be played on this device, and MIDI tracks recorded from the device can be played on computer. 

System requirements

Hardware:

Atmel STK500 starter kit (http://www.atmel.com/tools/stk500.aspx)
ATmega644 microcontroller (http://www.atmel.com/Images/doc2593.pdf)
STUDIOLOGIC MIDI keyboard (model: CMK137)
SD Card (2-8Gb formatted as FAT32)
Program developed by C/C++: see attached code for details.

Features:

A complete FAT system was established and the program provides the menu for different operations, including play, record and check SD card status. User can navigate the whole system by pressing the buttons. Please see Figure 1 for more details. 
Check SD card
When the device is on, first thing is to check if SD card is detected and the SD card has a format of FAT32. If not, the program stops. If yes, program proceeds to main menu, which includes Record, Play and SD Card.
Record
Selecting Record option will start recording immediately. User can record music by playing the keyboard. User is able to hear the sound he/she is playing while the MIDI track is written into SD card. When user finishing recording, he/she has the option to save or not save the MIDI track.
Play
On the LCD screen, user can choose the file he/she wants to play. The playing can be paused or stopped. After finishing playing the file, system is back to file list.
SD card
In this menu, user can check the size of each file, delete the file or check the free/total size of the SD card.

References

1. STK500 User Guide (http://www.atmel.com/Images/doc1925.pdf)
2. ATmega644 instruction (http://www.atmel.com/Images/doc2593.pdf)
3. AVR-LibC user manual (http://nongnu.org/avr-libc/user-manual/)
4. FAT32 system
http://msdn.microsoft.com/en-us/library/windows/hardware/gg463080.aspx
https://www.cs.drexel.edu/~jjohnson/2012-13/fall/cs370/resources/File%20Allocation%20Table.pdf
http://www.compuphase.com/mbr_fat.htm
http://www.pjrc.com/tech/8051/ide/fat32.html
5. AVRDUDE - AVR Downloader/UploaDEr (http://www.nongnu.org/avrdude/)
6. The Complete MIDI 1.0 Detailed Specification. The MIDI Manufacturers Association, Los Angeles, CA.
