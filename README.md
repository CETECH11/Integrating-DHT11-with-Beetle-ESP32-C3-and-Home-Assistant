# Integrating-DHT11-with-Beetle-ESP32-C3-and-Home-Assistant

![alt text](https://hackster.imgix.net/uploads/attachments/1683561/_SlN5lFulrp.blob?auto=compress%2Cformat&w=900&h=675&fit=min)

This project will allow you to monitor environmental conditions in your home automation setup. Here are the steps to achieve this:

1. Components Required

Before we begin, gather the necessary components:

BeetleESP32C3 development board
DHT11 temperature and humidity sensor
Jumper wires
USB cable for programming
A computer with the Arduino IDE or ESPHome installed

![alt text](https://hackster.imgix.net/uploads/attachments/1683704/image_hwgwkuf7fw.png?auto=compress%2Cformat&w=740&h=555&fit=max)

2. Flashing ESPHome to Beetle ESP32 C3
Install ESPHome on your computer. You can follow the instructions in my previous blog.
Create an ESPHome configuration file (e.g., dht11.yaml) with the following content:

```
sensor:
- platform: dht
pin: 0
model: dht11
temperature:
name: "Living Room Temperature"
humidity:
name: "Living Room Humidity"
update_interval: 5 s
```

Replace placeholders (YourWiFiSSID, YourWiFiPassword, etc.) with your actual values.
Compile and upload the configuration to your Beetle ESP32 C3 using the ESPHome CLI.

![alt text](https://hackster.imgix.net/uploads/attachments/1683713/image_r55UgZuUPN.png?auto=compress%2Cformat&w=740&h=555&fit=max)

3. Integrating with Home Assistant
Open Home Assistant.
Click on Configuration (bottom left) and go to Integrations.
Click the + button and select ESPHome.
Enter the IP address of your ESP32 (leave the port as 6053) and click Finish.


5. Viewing Temperature and Humidity
Once integrated, Home Assistant will discover the Beetle ESP32 C3 module and create entities for temperature and humidity.
You can access these entities in Home Assistant’s dashboard and display them as cards or graphs.
And that’s it! You’ve successfully integrated the DHT11 sensor with your Beetle ESP32 C3 and Home Assistant. Feel free to customize and expand this project based on your needs. Happy monitoring! 🌡️💧🏠

![alt text](https://hackster.imgix.net/uploads/attachments/1518136/8_tJuwoRM3dI.JPG?auto=compress%2Cformat&w=740&h=555&fit=max)

You must check out [PCBWAY](https://www.pcbway.com/) for ordering PCBs online for cheap!

You get 10 good-quality PCBs manufactured and shipped to your doorstep for cheap. You will also get a discount on shipping on your first order. Upload your Gerber files onto PCBWAY to get them manufactured with good quality and quick turnaround time. [PCBWay](https://www.pcbway.com/) now could provide a complete product solution, from design to enclosure production. Check out their online Gerber viewer function. With reward points, you can get free stuff from their gift shop.Also, check out this useful blog on PCBWay Plugin for KiCad from [here](https://www.pcbway.com/blog/News/PCBWay_Plug_In_for_KiCad_3ea6219c.html). Using this plugin, you can directly order PCBs in just one click after completing your design in KiCad.
