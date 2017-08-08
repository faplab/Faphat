# FapHat #
FapHat is a led strip controller board with an integrated battery charger and a serial adapter. It is compatible with the Arduino IDE.

## About the project ##
The goal of the project was to create an easily hackable, battery powered Arduino IDE compatible board for various projects. As we developed the project, we designed it to be able to run a WS2812b led strip for multiple hours. 18650 sized battery seemed suitable and the PCB design is based on the dimensions of that battery.

## Getting started ##
When you receive your FapHat, it should already contain the firmware and is ready to be used. However, if you want to modify the code or reflash the device, you can easily do that with Arduino IDE:

1. First you need to download the Arduino IDE from [https://arduino.cc] and install it.
2. FapHat uses the CH340G serial adapter, so make sure your operating system have drivers for that. Drivers might be available [here](http://sparks.gogo.co.nz/ch340.html).
3. Download the default firmware [here](https://github.com/faplab/faphat/tree/master/src/DemoReel100Sleep). Make a new Arduino project and copy the code there.
4. Select "Arduino Uno" as the board type in Arduino tools menu. Also select the correct usb port.
5. Then you can flash the firmware with the "Upload" button.

## More information ##
- The default firmare / demo reel uses the fastled library to animate the leds.
- The board uses optiboot bootloader.
- Some GPIO pins are exposed for your modifications / additions.

### Known limitations / bugs ###
- Arduino can not be programmed if battery charge is too low. Please let the device charge and/or disconnect the leds if the battery level is critical.
- Led strip drains battery even when there are no leds lit. Put device on sleep by pressing the button on the board and disconnect the led strip to spare the battery.

### Links ###
- [https://github.com/Optiboot/optiboot]
- [https://github.com/FastLED/FastLED]
