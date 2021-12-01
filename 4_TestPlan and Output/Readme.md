# TESTPLAN and OUTPUT
## Headers

* #include <avr/io.h>
* #include <MrLcd/MrLCDmega32.h>
* #include <avr/interrupt.h>
* #include <util/delay.h>
* #include <stdlib.h>
## Defining variables

* static volatile int pulse = 0;
* static volatile int i = 0;
The variable ‘pulse’ is used to store the count value from the TCNT register.
The variable ‘i’ is used as a flag to indicate the current status of the Echo pin.
## Initialisation of LCD and setting up of port D as IO port

* Initialise();
* DDRD = 0b11111011;
* _delay_ms(50);
* ‘Initialize()’ is a function used to initialize the LCD and is defined in the library of the LCD that has been previously made.

Next instruction sets up the function of the Pins of the port D of microcontroller. 1 means that an output device is connected at that PIN and microcontroller will write the logic there and 0 means that input device is connected there and microcontroller will read the logic from there.

“DDRD = 0b11111011”:

DDR Stands for “Data Direction Register”
D indicates PORTD of microcontroller
‘0b’ means binary
Each bit after 0b indicates the status of each pins of port in reverse order i.e PIND7, PIND6, PIND5, PIND4, PIND3, PIND2, PIND1, PIND0.
PIND2 is set as input pin as it is connected to the echo pin of the sensor. Thus the microcontroller will read the status of the echo PIN.
PIND0 is set to 1 as it is connected to trigger pin of the sensor. The microcontroller will trigger the sensor by setting up logic 1 and 0 at this pin.
We have used a few pins (PIND3, PIND4, PIND5) to connect the control pins of the LCD display. Thus to enable their use as output pins we have set them to logic high.
Other pins that are left open are don’t care pins and can be set at any value (i.e 0 or 1).
## Setting up the Interrupt

* GICR |= 1<<INT0;
* MCUCR |= 1<<ISC00;
* GICR : General Interrupt Control Registor
This Instruction is used to configure the PIN D2 as an interrupt PIN as the ECHO pin of the sensor is connected here.

MCUCR: MCU control Register
The second instruction defines that any logical change at the INT0/PIND2 Pin will cause the microcontroller.

Thus microcontroller will be interrupted when logic goes from 0 to 1 or from 1 to 0.






