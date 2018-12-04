# NFC Platform Build Instructions
My NFC platform is the Hardware project for Humber Collage course CENG317

## Author
Marko Javorac
Toronto,Canada

## Prerequistes
Due to the nature of this guide, a few skills will be required that are beyond the scope of this guide. A few helpful links are provided below to help you.

### Soldering
How to Solder / Soldering Basics Tutorial https://www.youtube.com/watch?v=BxASFu19bLU 
### Eagle
Tutorial 1 for Eagle https://www.youtube.com/watch?v=1AXwjZoyNno&t=0s
### CorelDraw
Full Tutorial for Beginners https://www.youtube.com/watch?v=iKfFNNtfpMU
### Raspberry Pi Guide
Getting Started with Raspberry Pi 3 https://www.youtube.com/watch?v=juHoJYX86Dg

## Budget
Review of total costs
https://github.com/markojavorac/nfc_platform/blob/master/documentation/Budget_v2.xlsx

## Hardware Required
PN532 Board + NFC Card https://learn.adafruit.com/adafruit-pn532-rfid-nfc
Soldering Station
PCB/PVC Printing
Protoypeing Equipment

## Software Required 
Developed for the Broadcom Development Platform (Raspberry Pi 3)
All relavent files required are provided in this repository

# Prototyping
![PN532](https://cdn-shop.adafruit.com/970x728/364-05.jpg)

#### Initial Hardware Configuration
To enable communicattion between the pi and the PN532 Board, You will have to choose a communications protocol and solder header pins on the designated protocol. For this tutorial we will be using I2C and jumpers will be needed to specify this protocol. The jumpers come in the PN532 kit.
![top side of sensor](https://github.com/markojavorac/nfc_platform/blob/master/resources/sensor_pin2.JPG)
![bottom side of sensor](https://github.com/markojavorac/nfc_platform/blob/master/resources/sensor_pin1.JPG)
![jumpers](https://github.com/markojavorac/nfc_platform/blob/master/resources/sensor_jumper.JPG)
#### NOTE!!!
To enable I2C or any other communication protocol, the jumpers must be configured correctly. Setup table is below.
![communications table](https://github.com/markojavorac/nfc_platform/blob/master/resources/i2c_config.png)

#### Initial Software Configuration
We will now be shifting our focus over to the sofware side.To interact with the board and use nfc functionality, we will be using and open source librarby named libnfc. The is a basic but powerful package of libraries that will get us going and be founcation to your future projects. We will again assume you understand how to setup and run debian on a raspberry pi

This official libnfc guide will walk you through installing the library. This website contains a plethora of information regarding NFC and should be your goto for troubleshooting the software side. 
### http://nfc-tools.org/index.php/Libnfc#Debian_.2F_Ubuntu

#### Bringing together initial hardware and software
We will give it quick test to make sure all our components are working. A breadboard is a great way to test this.

#### TODO hardware protoype

Running the nfc i2c detect protocol will let you know if your pi can actually see the i2c device. Your address might vary from mine and thats fine. The goal is just get an address.

![i2c detect](https://github.com/markojavorac/nfc_platform/blob/master/resources/nfc_sw1.png)

Using libnfc, we can run a simple poll program that when a card is detected, it will state simple information and confirm we can read nfc cards.

![i2c detect](https://github.com/markojavorac/nfc_platform/blob/master/resources/nfc_sw2.png)

### TODO!!!! 
Photos of development
i2c detect guide
pcb creation
case creation



## License
This project is licensed under the GNU General Public License v3.0 - see the LICENSE.md file for details

## Acknowledgments
- The undying support of my family and friends, in particular Jacob Ladan and Denald Demirxhiu. 
- All the faculty and support staff at Humber Collage
