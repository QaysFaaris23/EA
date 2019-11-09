# ESP32 Tutorial
How to install python on your ESP32 ?
Before we start make sure that you have the latest version of python installed on your computer.Here is a [link](https://www.python.org/downloads/) to install 

### Step 1

Download the Latest MicroPython Firmware
In this [link](https://micropython.org/download/#esp32), search for "esp32-idf3-20191109-v1.11-571-g7e374d231.bin", click and then download

### Step 2

Launch your command prompt on windows and enter the following 
```sh
pip install --upgrade esptool
```
<img src="https://github.com/QaysFaaris23/The-Engineering-Academy/blob/master/FaarisJOurnals/first%20cm%20pic.PNG" width ="700">

### Step 3

Next enter the following in the command prompt and it shoudl look like this
```sh
esptool.py --chip esp32 -p <USB-to-Serial Port> erase_flash
```
Before flashing the firmware to the ESP32, we'll want to erase everything in the chip's flash memory. To that, enter the following command (replace <USB-to-Serial Port> with your particular port name, such as COM7 on Windows, /dev/tty.usbserial-<letters and numbers> on macOS, or /dev/ttyUSB0 on Linux):
<img src="https://github.com/QaysFaaris23/The-Engineering-Academy/blob/master/FaarisJOurnals/second%20cm%20pic.PNG" width ="700">

### Step 4

Next enter the following in the command prompt and it should look like this
```sh
esptool.py --chip esp32 -p <USB-to-Serial Port> write_flash -z 0x1000 <path to .bin>
```
Flash the firmware with the following command (replace <USB-to-Serial Port> with your particular port name, and replace <path to .bin> with the location of your downloaded firmware file, such as ~/Downloads/esp32-20180822-v1.9.4-479-g828f771e3.bin):
<img src="https://github.com/QaysFaaris23/The-Engineering-Academy/blob/master/FaarisJOurnals/third%20cm%20pic.PNG" width ="700">

#YOU ARE ALL SET AND FINISHED! THANK YOU FOR READING







