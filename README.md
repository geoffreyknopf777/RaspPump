# RaspPump
A Raspberry Pi inspired pumpkin which lights up and has an evil laugh if you get too close

## Hardware Components
Raspberry Pi 2 Model B (qty. 1)

Sonar HC-SR04 (qty. 1)

LED (qty. 1)

1kOhm resistors (qty. 3)

## Software Modules
main.py - Invokes sonar.py to figure out how far away a person is. If they get too close, it blinks an led with led.py and plays an evil 
laugh with laugh.sh

led.py - Controls an led with a single GPIO pin

sonar.py - Sends a trigger pulse to the sonar and measures the duration of the echo pulse to determine distance

laugh.sh - Plays an evil laugh sound file
