# OTA-using-ESP32

### Step1:
Install the ArduinoOTA library for ESP32 on the Arduino IDE

### Step2:
* Go to the examples->ArduinoOTA->Basic OTA

### Step3:
* The ESP32 is much more secure than the ESP8266 , it is possible to store the hash of the password in place of it. To create your password fingerprint, you can use an online generator such as this one. For example, the hash of the admin password will give the fingerprint 21232f297a57a5a743894a0e4a801fc3.

* Then, use the setPasswordhash function instead of setPassword () to specify the authentication password.
ArduinoOTA.setPasswordHash("21232f297a57a5a743894a0e4a801fc3");
 
### Step4:
##### Wireless Update Test
* Upload the program and open the Terminal to verify that the ESP32 is properly connected to the Wi-Fi network.

* The Arduino IDE automatically detects devices that support remote update. They are added to the list of ports in a new section called Network ports.

* To update the program, simply select the ESP as the port instead of the usual serial port. Then upload the program as usual. Here, as a password is required, an input window appears in the IDE. It is requested only once

**Note:** This Code runs for only once i.e, update takes only for the first time and for the second time ESP network Does not work.

To run OTA for further updates 
```
Void setup()
{
	//include OTA setup needs
	//include your Setup needs
}
Void loop()
{
 	//include OTA request check
	//your loop  requirements
}
```

