# ESP8266_Weather_System_MicroUSB
ESP8266 Weather System using the MicroUSB connector

The project was originally created by Dani at: http://blog.squix.ch/2015/07/weatherstation-kit-complete-setup-guide.html
I loved this project and created a custom PCB for it. He also has written up and excellent install procedure.

Programming the Weather System Board

A. Install Arduino IDE

1. Go to https://www.arduino.cc/en/main/software
2. Download and install the Arduino IDE version 1.6.5


B. Add ESP8266 Support to Arduino IDE

1. Start the Arduino IDE
2. Go to File/Preferences
3. In the "Additional Board Manager URLs:" box enter http://arduino.esp8266.com/package_esp8266com_index.json
4. Click "OK"
5. Go to Tools/Board/Boards Manager
6. In "Filter your search..." box enter ESP
7. Click "esp8266 by ESP8266 Community" to select it
8. Click "Install"
9. Go to Tools/Board
10. Click "Generic ESP8266 Module"

C. Install ArduinoJson Library

1. Go to https://github.com/bblanchon/ArduinoJson
2. Click the "Download ZIP" button on the right
3. In the IDE, go to Sketch/Include Library/Add .ZIP Library
4. Select the ArduinoJson .zip file
5. Go to Sketch/Include Library
6. Select the ArduinoJson library (you should see it way down the list)
7. In the IDE, go to Sketch/Include Library/Manage Libraries
8. In the "Filter your search..." box enter "Adafruit SSD1306"
9. Click "Install"

D. Register for a free Weather Account

1. Go to https://developer.forecast.io
2. Click on "Register"
3. Create account
4. Register for free and create a weather account at https://developer.forecast.io
5. Copy down the API Key

E. Programming and Configuring the Board

1. In the IDE, go to File/New
2. File/Save As to "weather-station-v2" (this creates a subdirectory of the same name)
3. Go to https://github.com/squix78/esp8266-projects
4. Click on "Download ZIP"
5. Extract contents of downloaded zip to a temporary location
6. Find subdirectory weather-station-v2 and copy contents to Arduino subdirectory weather-station-v2
7. In the IDE, go to File/Open
8. Select the weather-station-v2.ino
9. Enter your SSID and password after line 50 //note that your weather-station-v2.ino is different from the one on squix//
10. Enter your forecastApiKey
11. Enter your latitude and longitude from http://maps.google.com/ and noting the lat & long in the top address
12. In the IDE click the checkmark button to see if it compiles without an error
13. If no errors then, press and hold the little pushbutton
14. While holding pushbutton, plug it into a USB port
15. Wait 2 seconds and release the button
16. In the IDE it should see it and auto install the driver
17. Tools/Port, select the new com port and then the Right Arrow (Upload button)
18. A bunch of little dots will pop up if it is successfully being programmed