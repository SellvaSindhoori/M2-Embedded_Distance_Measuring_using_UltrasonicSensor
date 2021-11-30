# Requirements

Ultrasonic sensors can measure the distance to a wide range of objects regardless of shape, color or surface texture. They are also able to measure an approaching or receding object. By using “non-contact” ultrasonic sensors, distances can be measured without damage to the object. They’re easy to use and, in many cases, can be used in place of other traditional sensors when the environmental conditions make traditional sensors unusable.

## Introduction
Migatron ultrasonic sensors can detect the distances to a variety of objects ranging from small spheres to large rolls of steel, and from bulk material on a conveyor belt to the liquid level in a storage tank and countless other distance measurements applications that need an ultrasonic sensor to get the job done. Ultrasonic distance measurement sensors are used in a wide array of industries like petroleum, chemical and manufacturing. Some examples of industry uses are roll diameter (either wind or unwind), bulk material conveyors and hopper/feeder level control.
## Research
The basic principle of ultrasonic distance measurement is based on ECHO. When sound waves are transmitted in the environment then waves return back to the origin as ECHO after striking on the obstacle. So we only need to calculate the traveling time of both sounds means outgoing time and returning time to origin after striking on the obstacle. As the speed of the sound is known to us, after some calculation we can calculate the distance. We are going to use this same technique for this Atmega 328 distance measurement project, so let's get started.  

## Features
The sensor module consists of an ultrasonic transmitter, receiver and control circuit. The working principle of ultrasonic sensor is as follows:

   * High level signal is sent for 10us using Trigger.
   * The module sends eight 40 KHz signals automatically, and then detects whether pulse is received or not.
   * If the signal is received, then it is through high level. The time of high duration is the time gap between sending and receiving the signal.
## Defining our System
he module works on the natural phenomenon of ECHO of sound. A pulse is sent for about 10us to trigger the module. After which the module automatically sends 8 cycles of 40 KHz ultrasound signal and checks its echo. The signal after striking with an obstacle returns back and is captured by the receiver. Thus the distance of the obstacle from the sensor is simply calculated by the formula given as

            Distance= (time x speed)/2.

Here we have divided the product of speed and time by 2 because the time is the total time it took to reach the obstacle and return back. Thus the time to reach obstacle is just half the total time taken.
## SWOT Analysis
### Strength
* Not affected by color or transparency of objects
* Can be used in dark environments
* Low-cost option
* Not highly affected by dust, dirt, or high-moisture environments
## Weakness
* Cannot work in a vacuum
* Not designed for underwater use
* Sensing accuracy affected by soft materials

## Opportunity
* They have greater accuracy than many other methods at measuring thickness and distance to a parallel surface
* Their high frequency, sensitivity, and penetrating power make it easy to detect external or deep objects
* Our ultrasonic sensors are easy to use and not dangerous during operation to nearby objects, people or equipment.
* Our sensors easily interface with microcontrollers or any type of controller.
## Threats
* Limited testing distance
* Inaccurate readings
* Inflexible scanning methods. 
## High Level Requirements
|RID|DESCRIPTION|STATUS|
|-----:|-----:|-----:|
|HLR1| ATMEGA 328|Implemented|
|HLR2| C language|Implemented|
|HLR3| Arduino IDE|Implemented|

## Low Level Requirements
|RID|DESCRIPTION|STATUS|
|-----:|-----:|-----:|
|LLR1| Ultrasonic Sensor|Implemented|
|LLR2| Distance measured|Implemented|
|LLR3| LCD Display|Implemented|

## 4W's and 1'H
### Why:
The main concept of building this project is to easily detect the preset range and generate an output signal.
### What:
This project is all about the alert system towards the independent of target size, material or reflectivity.
### Where:
This project is to calculate the  precise distance(s) of an object moving to and from the sensor are measured via time intervals between transmitted and reflected bursts of ultrasonic sound. 
### When:
This project is going to be deployed on 2/12/2021.
### How:
With Ultrasonic Sensing’s unique advantages over conventional sensors and the rapidly increasing range of applications, ultrasonic sensors are becoming widely accepted as an industry standard across the board.
