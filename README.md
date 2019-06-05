# GPS-Tracking-with-NodeMCU
An IoT project that monitors the real time location of GPS interfaced with Node MCU. The Node MCU receives the data from the GPS the results can be viewed on Blynk mobile application by interfacing with ESP8266 Wi-Fi module present on Node MCU.

Just run the file in Arduino IDE with the given connections.

Working:
The GPS Module will transmit data in multiple strings at 9600 Baud Rate. If we use an UART terminal with 9600-Baud rate, we will see the data received by GPS. GPS module sends the Real time tracking position data in NMEA format. NodeMCU is ESP8266 based development board. It features ESP-12E as its processing core. It is a 32-bit MCU. It has 14 GPIO pins, single channel 10 bit integrated ADC. It supports UART, I2C, and SPI communication. It is 3.3V compatible, it cannot handle 5V. Blynk can control Digital and Analog I/O Pins on you hardware directly. The Virtual Pins are designed to send any data from your microcontroller to the Blynk App and back. GPS module takes some time to capture location details once it is powered on. NodeMCU starts webserver and waits for a client to be connected to the webserver over Wi-Fi. Once client is connected to the webserver, NodeMCU sends location details to connected client. The location details are displayed in the Blynk mobile application.


    Virtual Connections of the GPS and Blynk App-
    Virtual Pins      Application
        V0            Map Widget
        V1            Latitude
        V2            Longitude
        V3              Speed
        V4        Number of satellites
        V5            Direction
  
  
    The connections between Node MCU and GPS module is as shown below- 
    Node MCU        GPS module 
      3V3             Vcc 
      GND             GND 
      D1 (GPIO5)      RX 
      D2 (GPIO4)      TX
