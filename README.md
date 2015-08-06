# ESP8266_Weather_System_MicroUSB
ESP8266 Weather System using the MicroUSB connector

The project was originally created by Dani at: http://blog.squix.ch/2015/07/weatherstation-kit-complete-setup-guide.html
I loved this project and created a custom PCB for it. He also has written up and excellent install procedure.

Programming the Weather System Board

Setup
-go to https://www.arduino.cc/en/main/software, download and install the IDE version 1.6.5
-in the IDE go to File, preferences, Additional Board Manager URLs enter: http://arduino.esp8266.com/package_esp8266com_index.json
-in Tools, Boards, Boards Manager, in Filter Type in ESP, click it and install that Board
-now in Tools, Board click Gerneric ESP8266 Module

-install the ArduinoJson Library
-go to https://github.com/bblanchon/ArduinoJson and click the Download Zip button to the right
-in the IDE, Sketch, Include Library, Add .ZIP Library, select the ArduinoJson .zip file
-now in the IDE click Sketch, Include Library, you should see ArduinoJson way down the list

-figure out your Wifi SSID and password
-register for free and create a weather account at https://developer.forecast.io/
-copy your API Key down

Programming the Board
-download the code from here: https://github.com/squix78/esp8266-projects
-File, Open .ino file
-enter your SSID and password after line 50
-enter your forecastApiKey
-enter your latitude and longitude from http://maps.google.com/ and noting the lat & long in the top address
-in the IDE click the checkmark button to see if it compiles without an error
-if no errors then 

-press and hold the little pushbutton
-while holding plug it into the a USB port
-wait 2 seconds and release the button
-in the IDE it should see it and auto install the driver
-Tools, Port, select the new com port and then the Right Arrow(Upload button)
-a bunch of little dots will pop up if it is successfully being programmed

