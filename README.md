# Arduino-Cli-Using-NodeMCU
Arduino Cli files for compile and upload 

Step1: Download the setup file
Step 2: Move the file to a path e.g.  users/appdata/local/bin
Step 3: Connect nodemcu board to PC.
Step 4: Run terminal/cmd in the same directory you moved the file and write "arduino-cli core update-index" then hit enter.
Step 5: Create a .yml file and place in the same directory.File includes: 
        board_manager:
          additional_urls:
            - http://arduino.esp8266.com/stable/package_esp8266com_index.json
            
Step 6: Run on the cmd/terminal :
        arduino-cli core update-index;
        arduino-cli core install esp8266:esp8266
        
Step 7: Create a folder and give the same name as your scratch file name. (Arduino file. e.g LowerSensor)

Step 8: Run on cmd/terminal: (MyFirstSketch is folder name)
        arduino-cli compile --fqbn esp8266:esp8266:nodemcu MyFirstSketch
        
Step 9: Run on cmd/terminal: (com5 is port works on windows only)
        arduino-cli upload -p com5 --fqbn esp8266:esp8266:nodemcu MyFirstSketch
        
        
