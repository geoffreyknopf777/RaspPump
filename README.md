# RaspPump
A Raspberry Pi inspired pumpkin which lights up and has an evil laugh if you get too close

## Getting Started

Materials: Pumpkin, Raspberry Pi 2 B, HC-SR04 sonar, LED, Resistors, mini breadboard, jumper wires, speaker with headphone jack connector

If you've never carved a pumpkin before, here's a good place to start https://www.wikihow.com/Carve-a-Pumpkin

Follow the instructions at https://www.modmypi.com/blog/hc-sr04-ultrasonic-range-sensor-on-the-raspberry-pi for connecting the HC-SR04 sonar to the Raspberry Pi. This project assumes TRIG is connected to GPIO pin 23 and ECHO is connected to GPIO pin 24.

Follow the instructions at https://thepihut.com/blogs/raspberry-pi-tutorials/27968772-turning-on-an-led-with-your-raspberry-pis-gpio-pins for connecting an LED to the Raspberry Pi. This project assumes the LED is connected to GPIO pin 25. 

### Installing

Boot up the Raspberry Pi and open up a terminal. Clone this project into whatever directory you like.

```
git clone www.github.com/geoffreyknopf777/RaspPump
```

To run the program

```
cd RaspPump
sudo python main.py
```

To configure this program to run automatically whenever the Raspberry Pi boots, edit the /etc/rc.local file

```
vim /etc/rc.local
```

and add the following line

```
python <path>/main.py
```

Reboot the Pi to observe the program running automatically

```
sudo reboot
```

## Software Modules
main.py - Invokes sonar.py to figure out how far away a person is. If they get too close, it blinks an led with led.py and plays an evil 
laugh with laugh.sh

led.py - Controls an led with a single GPIO pin

sonar.py - Sends a trigger pulse to the sonar and measures the duration of the echo pulse to determine distance

laugh.sh - Plays an evil laugh sound file

## Built With

* [Raspberry Pi 2 Model B](https://www.raspberrypi.org/products/raspberry-pi-2-model-b/) - target hardware
* [HC-SR04](http://www.micropik.com/PDF/HCSR04.pdf) - ultrasonic ranging module

## Authors

* **Geoffrey Knopf** - *Initial work* - [geoffreyknopf777](https://github.com/geoffreyknopf777)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## References

* Sonar - https://www.modmypi.com/blog/hc-sr04-ultrasonic-range-sensor-on-the-raspberry-pi
* LED - https://thepihut.com/blogs/raspberry-pi-tutorials/27968772-turning-on-an-led-with-your-raspberry-pis-gpio-pins
* Audio - https://raspberrypi.stackexchange.com/questions/49672/how-to-play-mp3-on-background-from-command-line

## Acknowledgements

* Inspiration from going to the pumpkin patch with my girlfriend
