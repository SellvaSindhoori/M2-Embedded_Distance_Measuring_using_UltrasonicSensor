# REPORT
## Introduction
This project uses an ultrasonic sensor to indicate the distance of any object from it. Here we have made a setup based on a microcontroller in which real time distance is sensed by an ultrasonic sensor and displays measured distance on an LCD display.

## Required Components
* ATmega32 Microcontroller
* HC-SR04 Ultrasonic Distance Sensor
* 16×2 LCD Display
* 5V Power Supply
## Circuit Description
The overall circuit assembled on the breadboard contains three major components :ATmega 32 Microcontroller, Ultrasonic distance sensor and 16X2 Alphanumeric LCD display. The microcontroller is interfaced with 16X2 LCD and Ultrasonic sensor.

## HC-SR04 Ultrasonic Sensor
The ultrasonic distance sensor has 4 Pins: Vcc, GND, Trigger and Echo. The Vcc and GND are used to power up the sensor and are connected to power and ground rails on breadboard. Trigger is connected to PIN 14 (RX/PD0) and Echo is connected to PIN 16 (INT0/PD2) of the microcontroller.
## 16X2 LCD Display
There are various ways to interface the LCD display to microcontroller based on the coding technique and the platform used.
The LCD has 16 pins.

Pin no 1 and 2 are GND and Vcc respectively, and are used to power up the LCD.

The Pin no 3 VEE, which can be used to adjust the contrast of LCD by varying the potentiometer. We shall connect it to ground in our setup.

Pin no 4, 5 and 6 are the control pins of LCD and they decide the working of LCD. We shall connect these pins to PORT D of microcontroller.

Pin 4 is RS (Register Select) and is connected to PIN 17 (PD3/INT1),
Pin 5 is RW (Read / Write) and is connected to PIN 18 (PD4) and
Pin 6 is E (Enable) which is connected to PIN 19 (PD5) of the microcontroller.
Pin 7 to 14 are D0-D7 which are the data lines. They are connected to PORT A of the microcontroller (PIN 40-13).

The pin 15 and 16 are for LCD back light and those pins will be connected to Vcc And Gnd.
