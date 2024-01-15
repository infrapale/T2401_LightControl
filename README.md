# T2401_LightControl
This is an overview of my light control solution. The code and sketches will be saved in dedicated repositories
## Repositories
* https://github.com/infrapale/T2401_LightControl
* https://github.com/infrapale/T2401_KeyToRfm
* https://github.com/infrapale/T2312_Keypad_2x4
* https://github.com/infrapale/T2311_RFM69_Modem

## System overview

![overview pic](/images/Overview_1.png)

### 2x4 Keypad(s)
* Scan keys 1/10ms
* Send On message if pressed shortly 
* Send Off message if pressed longer

### Key to RFM69 Controller
* Receive and bufferkey messages 
* Map keys to a function or a group of functions
* Send (UART) function messages with appropriate interval for the RFM69 module

### RFM69 Modem
* Receive UART messages to be transmitted 
* Convert messages into JSON format when required
* Receive and save radio messages 
* Indicate when a message is available
* Send and decode radio message, to the UART

### RFM69 Receiver
* Dedicated relay message function

### Relay Unit
* Receive relay messages and control relay
## Implementation
### 2x4 Keypad
* Arduino Pro mini 3.3V 8MHz
* Arduino IDE
* PCB connecting the 8 Cherry MX type keys to the MCU
* Buffered Serial interface
### Key to RFM69 Controller
* Raspberry Pi Pico (W)
* Wifi is currently not used
* Arduino IDE single core
* Currenty on a prototype board
### RFM69 Modem
* Arduino Pro Mini 3.3V 8Mz
* RFM69 module with a 17cm wire antenna (SPI)
* Built on my own (old) PCB design
* Arduino IDE
### RFM69 Receiver
* Similar as the RFM69 Modem
### Relay Unit
* To be documented
* Different solutions for 230V AC and 12V
* 
