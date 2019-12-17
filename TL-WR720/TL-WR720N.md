On tplink router TL-WR720N v4, firmware version
3.17.1 Build 131021 Rel. 36123n has an arbitrary file reading vulnerability that does not require authentication
![images](https://github.com/WhooAmii/iot/blob/master/TL-WR720/1.png)
The cause of this vulnerability is because a path loginFs that anyone can call has been added to the httpd function through the httpCtrlConfAdd
function, and the processing function of this path did not properly handle the "../" input

Vulnerable Program：httpd
Firmware link：
We can't download v4 firmware from the official website of tplink. I analyzed by removing the firmware from the device. 


![images](https://github.com/WhooAmii/iot/blob/master/TL-WR720/2.png)
