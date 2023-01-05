This folder contains compiled OpenGarage firmware files.

To use OTA (over-the-air) update:

* Please note to upgrade to Firmware 1.2.0 and above you need to have ESP8266 WiFi chip with 4MB flash. The very early versions of OpenGarage (v1.0 and v1.1) unfortunately do not qualify as they only have 2MB flash. All later versions (v1.3, v1.4, v2.0 and above) have 4MB flash. Please also note that upgrading from earlier firmwares to firmware 1.2.0 ***will trigger*** a factory reset (due to flash memory layout changes). You are advised to copy/write down your existing settings before proceeding with the firmware update. 

* If you are not sure which version of the ESP8266 chip you have, you can upgrade to firmware 1.1.3 first, then once you are on 1.1.3, you can open a browser and type in
http://og_ip/db
where og_ip if your OpenGarage's IP address (or, if your OpenGarage is in AP mode, use http://192.168.4.1/db)
this should print out a JSON string in the browser and the last variable 'flash_size' is your flash memory size. If it's 4194304 then you have 4MB flash and can upgrade to firmware 1.2.1. Otherwise, if it's 2097152, then unfortunately it's not upgradeable to firmware 1.2.1.

* Download the specific firmware file (e.g. og_x.x.x.bin)

* Before uploading, close the Blynk and OpenGarage app if you use either of them, to avoid them interfering with the upload process.
  
* On your OpenGarage's web interface, click 'Update' at the bottom of the homepage. Select the firmware og_x.x.x.bin file, type in device key, and 'Submit'. Wait till it finishes.
  
* If the upload fails for any reason, you can try again. If the device hangs, unplug and plug back power and try again.
  
* If the firmware upload is corrupted for any reason, causing the device to fail to boot, you will need to re-upload the firmware using a microUSB cable. See README.md at the root folder for instructions.
