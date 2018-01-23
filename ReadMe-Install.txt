

Uploading the controller firmware is done in two steps, we need to upload the micrcontroller code followed by the files used for the web side of things



Steps:


********************************************************************** Step:1  Install Arduino ***************************************************************************************
-Download arduino IDE [or check that you have version 1.8.4 or later]


********************************************************************** Step:2 Install ESP8266 Addon *********************************************************************************
-Install the dependancies for ESP8266, guide can be found here: https://github.com/esp8266/Arduino
                        
                                        Start Arduino and open Preferences window.
                                        Enter http://arduino.esp8266.com/stable/package_esp8266com_index.json into Additional Board Manager URLs field. You can add multiple URLs, separating them with commas.
                                        Open Boards Manager from Tools > Board menu and install "esp8266" platform 

********************************************************************** Step:3 Install Esp8266 Spiffs Addon **************************************************************************
-https://github.com/esp8266/arduino-esp8266fs-plugin

Once that is done restart the arduino IDE, and the spiffs data upload option should be under tools tab

********************************************************************** Step:4 Uploading Spiffs Image **************************************************************************
-Extract main file and navigate to any .ino file, clicking will open in arduino IDE [Multiple tabs should be shown]
-save-as arduino sketch somewhere that you wont deleet it by accident
-In arduino IDE  Tools>Board>NodeMCU1.0   Tools>Port --Select the most likley port your nodemcu is on
-In arduino IDE Click compile, if you get a library error:
                              -
     
**********************************************************************Uploading Arduino Code **************************************************************************                          -
-Updating the IOT Side:
                           -In arduino IDE: Tools>Sketch DataUpload [If this option isnt shown go back to step 2-3] 
                            -updload takes around 120 seconds [Note you cant have serial open]

**********************************************************************Checking Upload was sucessful  **************************************************************************
-In Arduino IDE: Open Serial monitor Baud rate:115200  and click reset button on the NodeMCU
            -You should see some data [loading of eeprom, iot etc]

-if all that looks good, unplug the usb, plug it into the mains power. Wait 60 seconds and press the controller button. It should actuate ?


**********************************************************************Using Controller **************************************************************************
To Use: 
-Power On Controller
-On mobile/pc search for new controller Wifi hotspot and connect
-Open Chrome/similar and in the adress bar type  www.C.com 

If controller misbehaves or lost wifi password: Power on the unit, as soon as the blue LED lights hold the controller button for 60 seconds -- this will set the controller back to new
