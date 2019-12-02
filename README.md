# GoDirect
Vernier GoDirect modifications
This is code to work with the Vernier GoDirect CO2 sensor and integrates it in with the other NerdFarm code.
GoDirect is a 'push' model where the sensor pushes out data, you cannot 'pull' a single reading on demand.  Proper integration is still a work in progress.

Technical notes of commands and operation and from:
https://vernierst.github.io/godirect-examples/python/

Install the GoDirect library and dependencies with:
pip3 install godirect[USB,BLE]

The code is for using the sensor via a USB cable, or Bluetooth (BLE).  The code here is for USB

Raspberry Pi has an ownership issue with a low level function, see the documentation here:
https://vernierst.github.io/godirect-examples/python/godirect-py-faqs.html

vstlibusb.rules is in this repository, move it to the proper location with this code (note, the file path may need to be added)

sudo cp vstlibusb.rules /etc/udev/rules.d/.

The GoDirect Python library is included in this repository, and should be placed with your other Python code for the project (/home/pi/MVP/python)
