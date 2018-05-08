# ArduinoSmartDoorbell
An Arduino MKR1000 WiFi Smart Doorbell (based on standard dutch doorbell installation)

## Why?
* As fun project. To learn Arduino, electronics, programming, git etc.
* Current Smart Doorbells are expensive, have limitations and are often subscription based
* Don't want to change the current, standard doorbell installation too much
* Expand with an IP Camera wich does double duty for security

## User Requirements
* Use a button to ring the bell
* Detect the use of the button (and communicate it into the network for home automation)
* No internet dependancy (so no cloud services)
* Inexpensive hardware
* Keep it simple
* Optional: Ring the chime remotely
* Optional: Control an outdoor light


## Current installation
8V DC - Doorbell button - Chime

## Platform Options
ESP
Arduino
Particle 
etc. 
Chosen: Arduino MKR1000 WiFi. Others would work too I guess...

## Considirations
* The doorbell circuit is a different voltage then the Arduino
* Considering location, flexibility and performance WiFi is the connection of choise (instead of Ethernet, BTLE, LoRa, GSM)
* The doorbell circuit 
* I know very little about electronics

## Solutions
### 1. Arduino MKR1000 + relay + optocoupler 
Description
Use an optocoupler to detect the use of the button. Use the relay to controll the chime remotely (connected in parallel). 

Pro
* Doorbell function remains totally independant of the arduino's avalability
Con
* More components
* Complex
### 2. Arduino MRK1000 + relay
Description
Connect the doorbell button to the digital I/O of the arduino. Use relay to ring the chime locally and remotely.

Pro
* Most simple solution
Con
* Doorbell functionality depends on arduino availability. 
