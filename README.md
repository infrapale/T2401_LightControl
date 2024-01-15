# T2401_LightControl
This is an overview of my light control solution. The code and sketches will be saved in dedicated repositories

## System overview

![overview pic](/images/Overview_1.png)

**2x4 Keypad(s)**
* Scan keys 1/10ms
* Send On message if pressed shortly 
* Send Off message if pressed longer
**Key to RFM Controller**
* Receive and bufferkey messages 
* Map keys to a function or a group of functions
* Send (UART) function messages with appropriate interval for the RFM69 module
**RFM69 Modem**
* Receive UART messages to be transmitted 
* Convert messages into JSON format when required
* Receive and save radio messages 
* Indicate when a message is available
* Send and decode radio message, to the UART
**RFM69 Receiver**
* Dedicated relay message function
**Relay Unit** 
* Receive relay messages and control relay
