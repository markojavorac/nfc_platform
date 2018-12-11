# Adafruit PN532 NFC/RFID + PCB Build Instructions
By: Marko Javorac
Toronto, Canada
## Introduction
NFC/RFID technology has been a staple in the world for decades. From security to automation, this technology can implemented in a varity of ways. This guide will help you up and running using the Adafruit PN532 board with your Rasberry Pi.
![PN532](https://cdn-shop.adafruit.com/970x728/364-05.jpg)


## Prerequistes
Due to its nature, a few skills will be required that are beyond the scope of this guide. A few helpful links are provided below.
- Soldering Basics Tutorial https://www.youtube.com/watch?v=BxASFu19bLU 
- Eagle https://www.youtube.com/watch?v=1AXwjZoyNno&t=0s
- CorelDraw https://www.youtube.com/watch?v=iKfFNNtfpMU
- Raspberry Pi Guide https://www.youtube.com/watch?v=juHoJYX86Dg

## Budget
The toal cost of this project can very depending on how much equipment you have access to and the PCB providers.
A fulll breakdown of the costs is avaliable here. 
- https://github.com/markojavorac/nfc_platform/blob/master/documentation/Budget_v2.xlsx

## Hardware Required
- PN532 Board + NFC Card https://learn.adafruit.com/adafruit-pn532-rfid-nfc
- Soldering Station
- PCB/PVC Printing
- Prototyping Equipment

## Software Required 
- RaspianOS running on a Raspberry Pi Model 3

# Prototyping
#### Initial Hardware Configuration
To enable comunicattion between the Pi and the PN532 Board, you will have to choose a communications protocol and solder jumpers on the designated protocol. For this tutorial we will be using I2C. The jumpers are included in the PN532 kit.
![top side of sensor](https://github.com/markojavorac/nfc_platform/blob/master/resources/sensor_pin2.JPG)
![bottom side of sensor](https://github.com/markojavorac/nfc_platform/blob/master/resources/sensor_pin1.JPG)
![jumpers](https://github.com/markojavorac/nfc_platform/blob/master/resources/sensor_jumper.JPG)

#### I2C 
To enable I2C or any other communication protocol, the jumpers must be configured correctly. Setup table is below.
![communications table](https://github.com/markojavorac/nfc_platform/blob/master/resources/i2c_config.png)

#### Initial Software Configuration
We will now be shifting our focus over to the sofware side. To interact with the board and use nfc functionality, we will be using an open source library called libnfc. The is a basic but powerful package of libraries that will get us going and be foundation to your future projects. We will again assume you understand how to setup and run Debian on a Pi.

This official libnfc guide will walk you through installing the library. This website contains a plethora of information regarding NFC and should be your goto for troubleshooting the software side.
 - http://nfc-tools.org/index.php/Libnfc#Debian_.2F_Ubuntu

#### Bringing together initial hardware and software
We will give it quick test to make sure all our components are working. A prototyping breadboard is a great way to do this. The pins must be configured the right way for our sensor. Be extra careful as you do this to not damage you board.

- Pin01 --> 3.3V
- Pin03 --> SDA
- Pin05 --> SLC
- Pin06 --> GND 

![proto 1](https://github.com/markojavorac/nfc_platform/blob/master/resources/proto_1.JPG)
![proto 2](https://github.com/markojavorac/nfc_platform/blob/master/resources/proto_2.JPG)



Running the i2cdetect program will let you know if your PI can actually see the i2c device. Your address might vary from mine and thats fine. The goal is just get an address.

![i2c detect](https://github.com/markojavorac/nfc_platform/blob/master/resources/nfc_sw1.png)

Using libnfc, we can run a simple poll program that when a card is detected, it will state simple information and confirm we can read nfc cards.

![i2c detect](https://github.com/markojavorac/nfc_platform/blob/master/resources/nfc_sw2.png)


## PCB
Our PCB is designed in EAGLE and the file is provided in PCB folder of this repository. Notice that I went through multiple iterations of the PCB to get a design that worked for me. Unless you have a PCB printing station avaliable to you, You will have to use an online printing soultion. A quick look up online will help you find the right one. It is also possible to find PCB printers in your area. There are a variety of pros and cons to each that you willl have to decide for yourself.

![pcb schmatic](https://github.com/markojavorac/nfc_platform/blob/master/resources/sch_1.png).

You will have to solder headers and resitors where shows in the images below. Follow the soldering guide linked at the top.

![pcb top1](https://github.com/markojavorac/nfc_platform/blob/master/resources/pcb_top_1.JPG)
![pcb top2](https://github.com/markojavorac/nfc_platform/blob/master/resources/pcb_top_2.JPG)
![pcb top1](https://github.com/markojavorac/nfc_platform/blob/master/resources/pcb_bot_1.JPG)
![pcb top2](https://github.com/markojavorac/nfc_platform/blob/master/resources/pcb_bot_2.JPG)

### NOTE:
This PCB is not the final one provided in the repository. It has a modifcation so you don't need to drill and rewire as I had to. In the future, I will repost an image of the final one.

## Case
Although it it not necessary to have a case, protecting your hardware is a great idea. In this repo, there is a case design cad file that is to be used with a sheet of acrylic. It is not a perfect case but it will get the job done

## Bringing it all together.
You should now be able to combine the pcb, board, and PI onto one neat unit. 
![final1](https://github.com/markojavorac/nfc_platform/blob/master/resources/pcb_final_1.JPG)
![final2](https://github.com/markojavorac/nfc_platform/blob/master/resources/pcb_final_2.JPG)
![final3](https://github.com/markojavorac/nfc_platform/blob/master/resources/final_1.JPG)


# Wrapping up
By following these instructions, you should be able to get your own PN532 board working on the Rasberrry Pi and begin exploring NFC projects with confidence. If you have any comments or suggestions please email me at javorac.plus@gmail.com.

-Marko

## License
This project is licensed under the GNU General Public License v3.0 - see the LICENSE.md file for details

## Acknowledgments
- The undying support of my family and friends, in particular Jacob Ladan and Denald Demirxhiu. 
- All the faculty and support staff at Humber Collage
