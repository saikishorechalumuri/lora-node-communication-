# lora-node-communication-
Here in this project I created a Lora node and communicated a message to TTN network server via my node and view my data at network server side 
Introduction
LoRa is a long range, low power transmission protocol. It allows data to be sent long distances. (We were able to go three floors up in the Tannery with a gateway in the lab) The downside is that bandwidth is limited.
#HERE IN THIS  PROJECT I ASSUME YOU ALREADY HAD A GATEWAY SETUP #
MY LORA NODE CIRCUIT DIAGRAM 
![image](https://user-images.githubusercontent.com/93335682/177617429-f3765bfc-babe-4ba5-9274-7ab20bdc55ec.png)
The important parts of this sketch are as follows:

LORA Module Pin mapping: This part defines the extra pins used by the radio to communicate status.
10 pins MUST be connected to the radio for it to work; 2 power (VCC & GND), 3 SPI Pins (MISO, MOSI, SCK) and 5 control (RST, CS, G0, G1, G2). The SPI must be connected to the correct pins to work. The 5 control lines can be connected to any available digital pins (as long as you define them).  *Cannot be remapped
Radio		Arduino
VCC 	–	VCC
GND 	– 	GND
MISO	–	*D12
MOSI	–	*D11
SCK	–	*D13 
CS	–	D10
RST	–	D9
G0	–	D2
G1	–	D3
G2	–	D4
REFERENCE VEDIO HELPED FOR THIS COMMUNICATION SETUP 
1) https://www.youtube.com/watch?v=0uzGRoZNki0&feature=youtu.be

https://lora.readthedocs.io/en/latest/


OUTPUT IMAGES 
![image](https://user-images.githubusercontent.com/93335682/177617829-28525382-98d3-469a-b97a-a0d762977982.png)
AFTER DECODING THE PAYLOAD THE MESSAGE IN HEXT FORMAT TO STRING FORMAT 
OUTPUT IMAGE 
![image](https://user-images.githubusercontent.com/93335682/177617982-3357a873-9eea-47ed-abea-fe8266763176.png)
THEREFORE TO DECODE THE DATA IN TTN SERVER WE MUST WRITE THE DECODE SCRIPTS AND WRITE IN THE PAYLOAD FORMATERS OF TTN NETWORK 

IF YOU ARE USING THE SMART TECTELIC SMART  SENSORS THERE IS SOME THING WE MUST FOLLOW 

THE UPLINK ARE FOR SENSORS TO REPORT NETWORK SERVER THEY ARE SEND IN PORT 10 
THE DOWNLINKS ARE FOR NETWORK SERVER TO SENSOR & WHICH WILL BE SEND ON PORT 100
