# DrumPad
*I think everyone knows about DrumPAD and those who don't let me explain you*
*IT will have 9 strikable PADS which if struck by  a stick will play different notes on different PADS*

### why i made this ?
>HI , This time i will be building a Whole drum pad from scratch .It's just a random project i always wanted to build 
>IT Will teach me about how audio amplifiers work   
>How i can use them to run a Speaker which will have mono audios of Each drumPAD
>Will got to know about how conversion of Audio pack happens and how it will be converted to Sound arrays
>
>  Hope it turns the best 

## Project showcase :
<img width="35%" height="1078" alt="image" src="https://github.com/user-attachments/assets/e0f07862-8563-48b4-a98c-259255a65c08" /> <img width="35%" height="1078" alt="image" src="https://github.com/user-attachments/assets/b84e0c74-347e-4bf2-9661-60a082881c42" /> 
<img width="35%" height="901" alt="image" src="https://github.com/user-attachments/assets/8d553e56-3bc4-4d84-99ad-93765e71a391" /> <img width="35%" height="897" alt="image" src="https://github.com/user-attachments/assets/650e46fa-52d7-4da1-a130-4c2a50cccb29" />

## PHYSICAL specifications:  
  
**PCB OUTLINE:** 98mm x 59 mm  

**Copper traces:** USES 0.6mm width copper traces for Power lines and 0.254mm for Signal tracks 
  
**MOUNTING:** has 2 M3 screw holes  

**MICROCONTROLLER:** USING ESP32-S3 module  

**DISPLAY:** USES 0.96inch OLED  

**AUDIO:**  
  
-Uses smartelex-i2s-audio-breakout-max98357  
  
-A speaker of 2 Inch Mini Speaker Driver, 4 Ohm 3W

**Sensor:** USES piezo disc as drums   
  

**USER:** CAN Play a drumPAd with the drumsticks when Esp32-s3 is powered 


## PCB OVERVIEW:  
  
<img width="35%" height="537" alt="image" src="https://github.com/user-attachments/assets/fdee43da-8a00-4748-b18d-f61f4a946b12" /> <img width="35%" height="513" alt="image" src="https://github.com/user-attachments/assets/d90b83c9-74f2-42cb-9247-482df2c56340" />  
<img width="35%" height="927" alt="image" src="https://github.com/user-attachments/assets/728d2d9f-0300-4692-83df-3849765d6793" /> <img width="35%" height="926" alt="image" src="https://github.com/user-attachments/assets/0f4d9c49-f572-433c-9c75-75f5db1bb672" />

## WIRING DIAGRAM with schematic :
 
### REMEMBER THOSE PINS WHICH ARE NOT MENTIONED BELOW ARE NOT USED   

### Hardware Notes & Audio Configuration  
 
**MAX98357A SD Pin Note:** Depending on the specific amplifier breakout revision and channel configuration, the SD (Shutdown/Mode) pin state handles audio muting and mono/stereo selection. If you experience unexpected muting or background noise during testing, a jumper wire may be added to tie the SD pin directly to the 3.3V rail for stable active mono operation.

**ESP32-S3 pins :**   
  
>PAD1---->GPIO1  
>PAD2---->GPIO2  
>PAD3---->GPIO3  
>PAD4---->GPIO4  
>PAD5---->GPIO5  
>PAD6---->GPIO6  
>PAD7---->GPIO7  
>PAD8---->GPIO17  
>PAD9---->GPIO18  
>SCL----->GPIO9  
>SDA----->GPIO8  
>DIN----->GPIO13
>BCLK---->GPIO11
>LRCLK--->GPIO12
>SW(net port)---->GPIO14
>5V------>5V(net port)
>3V3----->VCC(net port)
>GND----->GND(net port)

**i2s-audio-breakout-max98357a pins :**  

>V+------> 5V(net port)  
>GND----->GND(net port)  
>DIN----->GPIO13
>BCLK---->GPIO11
>LRCLK--->GPIO12

**OLED 0.96inch pins :**

>VCC----->VCC(net port)  
>GND----->GND(net port)  
>SCL----->GPIO9
>SDA----->GPIO8

**PUSH BUTTON :**

>4(switch pin)----->GND  
>1(switch pin)----->SW(net port)  

**PAD (1 to 9) pins:**

>PAD+---->Resistor(1M ohm)---->PAD(//number of that PAD){port}  
>PAD- ---->Resistor(1M ohm)  
  
**polarized Capacitor(1000microferrate) pins:**

>CAP+---->5V(net port)
>CAP- --->GND(net port)

## SCHEMATIC OVERVIEW : 

<img width="50%" height="865" alt="image" src="https://github.com/user-attachments/assets/e73ad55c-1fa2-42f1-9c98-b0fa8ddbf134" />   

## 3D PART assembly :

**MAIN casing**:   
  
>PLACE MAIN PAD and mount your PCB with M3 screws and nuts  
>PLACE the piezo discs in the designated holes 
>PLACE the upper lid and secure it with M3 screws
>The wires coming from the PADS will be placed into the headers as per you want to mark each disc as your desired Pad number 
>Then secure the bottom PAD lid with M3 screws
>Then place the speaker in the main lid with its designated holes
>Then place the button in top Lid and now you are good to go

## Main casing overview:  
 
<img width="35%" height="898" alt="image" src="https://github.com/user-attachments/assets/77389d54-61ff-4bc2-8fe4-3b928159e0e2" /> <img width="35%" height="896" alt="image" src="https://github.com/user-attachments/assets/1fff33e3-6743-44ed-b749-59628758224d" />



**Other enclosures**:

> Take the bottom part where the PCB will enclose , secure it with M3 screws  
>PLace the top lid over it and secure it with M3 screws
> Place the button in top Lid
> Place your drumPad body and place all the piezo discs
> The wires coming from the PADS will be placed into the headers as per you want to mark each disc as your desired Pad number
> Place your bottom lid of drumPad and secure it
> After following all the steps you are good to go

## Other enclosure overview:

<img width="35%" height="900" alt="image" src="https://github.com/user-attachments/assets/1e6dc6e6-3988-4e77-83c0-bff0776b3b4d" /> <img width="35%" height="907" alt="image" src="https://github.com/user-attachments/assets/ef1a5b3c-20e7-4f4f-a0b8-0dcb91dae835" />
  
### Bill of Materials (BOM)

| Item | Qty | Supplier | Cost/Item ($) | Total Cost ($) | Link |
| --- | --- | --- | --- | --- | --- |
| **ESP-32-S3** | 1 | robu.in | $8.63 | $8.63 | [Link](https://www.google.com/search?q=https://robu.in/product/smartelex-esp32-s3-development-kit-m-1-1-pcs/%3Fgad_source%3D1%26gad_campaignid%3D18585959909%26gbraid%3D0AAAAADvLFWc45-oZO6cgk0EQswTIPcYto%26gclid%3DCjwKCAjw_9bWBhBGEiwAomyTIiLbVugLY-qoXiJKU1NRdYjlvNy5Le-YH--xj9MyMwJK56ZC2bRFDhoC1XYQAvD_BwE) |
| **SmartElex I2S Audio Breakout - MAX98357A** | 1 | robu.in | $2.04 | $2.04 | [Link](https://www.google.com/search?q=https://robu.in/product/smartelex-i2s-audio-breakout-max98357a/%3Fgad_source%3D1%26gad_campaignid%3D18585959909%26gbraid%3D0AAAAADvLFWc45-oZO6cgk0EQswTIPcYto%26gclid%3DCjwKCAjw_9bWBhBGEiwAomyTIlhAQQEx5eKc3236O3AF8oBiK3bvH5T5GiiI0qBz3UgBim7wRTp9exoC9CYQAvD_BwE) |
| **Piezo Discs** | 1 | amazon | $4.41 | $4.41 | [Link](https://www.google.com/search?q=https://www.amazon.in/pieces-color-Piezo-Discs-transducer-piezoelectric/dp/B07DH8X3KJ/) |
| **2 Inch Mini Speaker Driver, 4 Ohm 3W** | 1 | amazon | $1.78 | $1.78 | [Link](https://www.google.com/search?q=https://www.amazon.in/Speaker-Driver-Projects-Electronic-Devices/dp/B0GTZ5DD6P/) |
| **PCB** | 1 | lion circuits | $16.44 | $16.44 | [Link](https://www.lioncircuits.com/quote) |
| **1M ohm resistors** | 30 | robu.in | $0.01 | $0.30 | [Link](https://robu.in/product/1m-ohm-0-25w-metal-film-resistor-pack-of-100/) |
| **1000microfarad capacitor** | 1 | robu.in | $0.13 | $0.13 | [Link](https://robu.in/product/1000uf-25v-electrolytic-capacitor-dip-pack-of-5/) |
| **OLED Display Module** | 1 | robu.in | $3.15 | $3.15 | [Link](https://www.amazon.in/Compatible-Projects-Interface-Microcontroller-Electronics/dp/B0FDR9G461) |
| **M3 nylon screws and nuts** | 1 | robu.in | $1.64 | $1.64 | [Link](https://robu.in/product/m315mm-nylon-screw-50-pcs/) |
| **Female headers** | 1 | robu.in | $0.40 | $0.40 | [Link](https://robu.in/product/2mm-pitch-female-berg-strip-40x1-2pcs/) |
| **Push button** | 2 | robu.in | $0.10 | $0.20 | [Link](https://robu.in/product/6x6x5-tactile-push-button-switch/) |
| **Softline Pro SP DSG 5A Maple Wood Drumstick** | 1 | flipkart | $2.05 | $2.05 | [Link](https://www.flipkart.com/softline-pro-sp-dsg-5a-maple-wood-drumstick-percussion-instrument-1-pair-standard-drumsticks/p/itmd7dbda3c0af31) |
| **Foam sheet** | 1 | flipkart | $1.81 | $1.81 | [Link](https://www.flipkart.com/aicon-high-density-rubber-foam-sheet-expansion-joint-filler-anti-vibration-shock-absorbing/p/itm6529f10ec9351) |
| **Estimated total shipping** | 1 | Various | $3.00 | $3.00 | N/A |
| **TOTAL** |  |  |  | **$45.98** |  |


## License
This project is licensed under **CC BY-NC 4.0** (Creative Commons Attribution-NonCommercial). 
You are free to build and modify this board for personal use, but commercial production or selling of this project is strictly prohibited.








