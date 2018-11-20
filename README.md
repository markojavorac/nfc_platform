# NFC Platform
My NFC platform is the Hardware project for Humber Collage course CENG317

## Author
Marko Javorac
Toronto,Canada

## Hardware
PN532 Board
https://learn.adafruit.com/adafruit-pn532-rfid-nfc

## Software
Developed on and for the Broadcom Development Platform(Raspberry Pi)

## Budget
https://github.com/markojavorac/nfc_platform/blob/master/documentation/Budget_v2.xlsx

## Progress
[Project Schedule](temp.com)
### Week 9
PCB has been designed in Eagle and submitted to the prototype lab. Currently reading Beginning NFC by O'Reilly to understand libnfc and software standards.

### Week 10 - November 6th, 2018
Today is the PCB solder milestone. I plan to get my board from the prototype lab and create temporary connections to test if the board is functioning correctly.
I have lots of catching up to do in in this class as I missed the last two. This includes,
- [x] Re-upload budget
- [x] Pickup redesigned board
  * ~~Board is not wide enough and GPIO is hidden under the PN532~~
  * ~~Reduce GPIO's to top 6~~
  * ~~Remove copper plater to reduce shorting chances~~
  * ~~Widen lines to 15mm~~
  * ~~Redo PCB layout~~
- [ ] Cut/short I2C jumpers
- [x] Read the first 3 chapters of "Beginning NFC"
- [x] ~~Purchase stack header pins~~ + ~~add to budget~~
- [x] Add image of PCB
#### Image Update - PCB_V1
![Image of pcb_v1](https://github.com/markojavorac/nfc_platform/blob/master/resources/pcb_v1.JPG)

### Week 11 - November 13th, 2018
Today I picked up my board but with Kristians keen eye, he caught that my board had some fundamental design flaws. I will have to redo the wiring so that when I solder my headers, they will actually do something. I also need to begin on the case and start the backend of this project. I will have to work with Jacob to make sure our sensors can work together properly.
- [x] Rewire
- [x] Reprint
- [x] Start case
- [ ] Cut/short I2C jumpers

#### Image Update - PCB_V4
![Image of pcb_v4](https://raw.githubusercontent.com/markojavorac/nfc_platform/master/resources/pcb_v4_1.JPG)
![Image of pcb_v4_2](https://raw.githubusercontent.com/markojavorac/nfc_platform/master/resources/pcb_v4_2.JPG)

### Week 12 - November 20th, 2018
- [ ] Print case
- [ ] Cut/short I2C jumpers

## License
This project is licensed under the GNU General Public License v3.0 - see the LICENSE.md file for details

## Acknowledgments
- The undying support of my family and friends, in particular Jacob Ladan and Denald Demirxhiu. 
- All the faculty and support staff at Humber Collage
