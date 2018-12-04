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


## Hardware Required
PN532 Board + NFC Card https://learn.adafruit.com/adafruit-pn532-rfid-nfc
Soldering Station
PCB/PVC Printing
Protoypeing Equipment


## Software Required 
Developed for the Broadcom Development Platform (Raspberry Pi 3)
All relavent files required are provided in this repository

# Prototyping
img of board layout

#### Initial soldering
To enable communicattion between the pi and the PN532 Board, You will have to choose a communications protocol and solder header pins on the designated protocol. For this tutorial we will be using I2C and jumpers will be needed to specify this protocol. The jumpers come in the PN532 kit.
![top side of sensor](https://github.com/markojavorac/nfc_platform/blob/master/resources/sensor_pin2.JPG)
![bottom side of sensor](https://github.com/markojavorac/nfc_platform/blob/master/resources/sensor_pin1.JPG)
![jumpers](https://github.com/markojavorac/nfc_platform/blob/master/resources/sensor_jumper.JPG)
#### NOTE!!!
To enable I2C or any other communication protocol, the jumpers must be configured correctly. Setup table is below.
![communications table](https://github.com/markojavorac/nfc_platform/blob/master/resources/i2c_config.png)






##
## TODO 
Hardware required
Hardware assembly instructions
Photos of development
i2c detect guide
pcb creation



## Budget
https://github.com/markojavorac/nfc_platform/blob/master/documentation/Budget_v2.xlsx

## License
This project is licensed under the GNU General Public License v3.0 - see the LICENSE.md file for details

## Acknowledgments
- The undying support of my family and friends, in particular Jacob Ladan and Denald Demirxhiu. 
- All the faculty and support staff at Humber Collage
