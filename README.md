# LCD Text Display Project Without Potentiometer
Welcome to the LCD Text Display Project repository! This basic project demonstrates how to display text on an LCD screen using an Arduino microcontroller. It's a great starting point for beginners interested in learning how to interface LCDs with microcontrollers.
<p align="center">
  <img src="https://github.com/Iswarya-Singaram/LCD-Connection-In-Arduino/assets/145309713/e4bd805a-d4bd-4c27-a973-3b0b6eac6880" width="500" height="300">
</p>

## Overview
This project uses a 16x2 character LCD to display text.The code initializes the LCD, sets up the required pins, and displays a simple message. This project helps you understand the basics of working with LCDs and microcontrollers.
<p align="center">
  <img src="https://github.com/Iswarya-Singaram/LCD-Connection-In-Arduino/assets/145309713/c31e42b2-5617-4f51-99b8-4594de5ff5d4" width="500" height="300">
</p>

## Components Used
<ul>
<li>Arduino Microcontroller</li>
<li>16x2 Character LCD: Standard HD44780 LCD</li>
<li>Jumper Wires: For connecting the components</li>
</ul>

## Getting Started
To get started with this project, follow the instructions below:
### Hardware Setup
#### Connect the LCD to the Arduino:
1. VCC to 5V
2. GND to GND
3. V0 (Contrast) to the GND
4. RS to digital pin D12
5. RW to GND
6. E to digital pin D11
7. D4 to digital pin D5
8. D5 to digital pin D4
9. D6 to digital pin D3
10. D7 to digital pin D2
11. A (Anode, backlight) to 5V (with a resistor if necessary)
13. K (Cathode, backlight) to GND

 <p align="center">
  <img src="https://github.com/Iswarya-Singaram/LCD-Text-Display-Project-Without-Potentiometer/assets/145309713/d0584e79-bb23-410d-9898-08415b1563dd" width="500" height="300">
</p>

<p align="center">
  <img src="https://github.com/Iswarya-Singaram/LCD-Connection-In-Arduino/assets/145309713/5a43ceb4-3d87-4d36-a359-a66f8d425461" width="500" height="300">
</p>

Note: The resistor connected to the backlight anode is optional in real life implementation of the project

###  Software Setup
#### 1.Download the latest Arduino IDE from the official website
~~~
https://www.arduino.cc/en/software
~~~
#### 2.Downloading the LiquidCrystal display library
1. Open the Library Manager
2. Go to Sketch > Include Library > Manage Libraries...
   <p align="center">
  <img src="https://github.com/Iswarya-Singaram/LCD-Connection-In-Arduino/assets/145309713/2068df2a-1a64-4f2e-8a1d-d51c2338e2cd" width="500" height="300">
</p>

3. In the Library Manager, type LiquidCrystal into the search box.
5. Locate the LiquidCrystal library by Arduino.
6. Click on the Install button next to the library.

#### 3.Run the source code
Run the following source code
~~~
#include <LiquidCrystal.h> 
int Contrast=75;
 LiquidCrystal lcd(12, 11, 5, 4, 3, 2);  

 void setup()
 {
    analogWrite(6,Contrast);
     lcd.begin(16, 2);
  } 
     void loop()
 { 
     lcd.setCursor(0, 0);
     lcd.print("Hello");
   
    lcd.setCursor(0, 1);
     lcd.print("World");
 }
~~~
Note: Adjust the contrast value incase the LCD's brightness too dim 

