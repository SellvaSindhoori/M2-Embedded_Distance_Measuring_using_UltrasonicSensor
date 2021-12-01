# COMMUNICATION
## UART
In UART communication, two UARTs communicate directly with each other. The transmitting UART converts parallel data from a controlling device like a CPU into serial form, transmits it in serial to the receiving UART, which then converts the serial data back into parallel data for the receiving device.

The main function of UART is to serial data communication. In UART, the communication between two devices can be done in two ways namely serial data communication and parallel data communication.

The UART that is going to transmit data receives the data from a data bus.

 The data bus is used to send data to the UART by another device like a CPU, memory, or microcontroller. Data is transferred from the data bus to the transmitting UART in parallel form. After the transmitting UART gets the parallel data from the data bus, it adds a start bit, a parity bit, and a stop bit, creating the data packet.

 Next, the data packet is output serially, bit by bit at the Tx pin. The receiving UART reads the data packet bit by bit at its Rx pin. 
 
 The receiving UART then converts the data back into parallel form and removes the start bit, parity bit, and stop bits. 
 
 Finally, the receiving UART transfers the data packet in parallel to the data bus on the receiving end.

 Ultrasonic sensor will be having transmitter and receiver in it. Transmitter continuously transmits the signal and whenever obstacle approaches the  sensor then that transmitted signal hits the object, bounce back and received by ultrasonic receiver. 
 
 That sensor sensed signal with respect to distance is then send to microcontroller, microcontroller in turn displays the measured distance value on LCD.
