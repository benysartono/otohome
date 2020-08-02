# otohome
Do it yourself IOT device to control your households.
Here you will build an IOT device that will connect to the internet via WiFi at your home. This device will sens and send humidity and temperature data suround it.
You will be able to turn on/off, as well through this device.

Lets get start:

1. Prerequisite
    a. WiFi internet connection
    b. Microcontroller that has a WiFi feature. In this case we'll use WEMOS D1 Mini
    c. Humidity and Temperature sensor. In this case we'll be using DHT11 shield for WEMOS D1 Mini
    d. Relay. In this case we'll be using 5V VCC relay shield for WEMOS D1 Mini
    
2. Circuitry
    Arrange the circuitry as below:
    a. WEMOS D1 pin to Relay Shiled D1 pin
    b. WEMOS 5V pin to Relay Shiled 5V pin
    c. WEMOS Gnd pin to Relay Shiled Gnd pin
    d. WEMOS 3V3 pin to Relay Shield 3V3 pin
    e. WEMOS D4 pin to DHT11 Shield D4 pin
    f. WEMOS 5V pin to DHT11 Shield 5V on
    c. WEMOS Gnd pin to DHT11 Shiled Gnd pin
    d. WEMOS 3V3 pin to DHT11 Shield 3V3 pin
    e. You will use "NO" and "GND" pin in the relay to function your relay as a switch  
    
3. Software tools required
    a. Download the binary program sketch_otohome_20200802_v1.ino.d1_mini.bin from here:
    b. Installing Phyton 2.x.x
       You can find in this url link https://www.python.org/downloads/
    c. Installing esptool using pip 
        1. Open the folder in where you installed the python
        2. Under the folder find pip.exe file (normally it is in the Script folder)
        3. Open cmd shell and go inside the folder contains the pip.exe
        4. Execute this command: pip install esptool (it will install the esptool) 
     d. After the esptools got intalled:
        1. Plug your ESP8266 to your notebook through USB to COMX (X represent the port you connected to)
        2. Open the folder in where you installed the python
        3. Under the folder find esptool.py.exe file (normally it is in the Script folder)
        4. Open cmd shell and go inside the folder contains the esptool.py.exe
        5. Execute this command to upload the binary file to the device:  
            ./esptool.py --port COMX write_flash --no-compress 0x00000 sketch_otohome_20200802_v1.ino.d1_mini.bin
        6. Install OTOHOME android app from google play store
        
4. Configuration
   Configure your device to connect to the internet via the WiFi:
     a. Power on your device
     b. Using your mobile connect to the "SMARNOC_APP" access point created by the device
     c. Use password "smarnoc_app" 
     d. Using the mobile's browser, browse to http://192.168.11.6
     e. You be presented with a page with a form to fill up your home ssid and the password
     f. After filling up the form, you will be presented with a page contain MAC address of your device
     g. Take note the MAC address to be used when you manage your device later on
     
5. Sign up to the OTOHOME app to create your account by opening and clicking sign up link in the OTOHOME app, and follow the steps

6. Manage your device through your mobile
      a. Login to your OTOHOME app
      b. At the menu page, click "Manage Device"
      c. Register a new device by filling up the name and the MAC address
      d. Now you can turn your device On/Off as well as reading the Humidity and Temperature suround your device
      e. Note: by registering your device to OTOHOME, you are automatically subscribe to the OTOHOME cloud service
      f. You will be charged monthly payment 
      g. The monthly bill will be sent to your email
      h. Failing to pay 3 consecutive months bill will cause  termination to your subscribtion without notice
      i. Your subscribtion will continue after your pay your 3 months unpaid bills.
   
        
        

    
