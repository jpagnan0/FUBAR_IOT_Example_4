# Control WS2812 LED with MQTT

This is the ESP8366 code for receiving commands via MQTT to control LED.  We wil be using NodeRed on a Raspberry Pi as the UI.  The code expect a hex string that contains the color tuple.  Format is RGB_HexString, Example **_RGB0xffffff_** to turn on full brightness white.  Wiring is the same as the other WS2812 Led example.

Note: The client names, outgoing and incoming MQTT topics must be unique for this example to work properly.

Need to install the Mqtt helper library included in this repo. Also need the [PubSubClient](https://github.com/knolleary/pubsubclient), Captive portal [WifiManager](https://github.com/tzapu/WiFiManager), and [FastLed](https://github.com/FastLED/FastLED) libraries installed using the PIO library manager.

Raspberry Pi Pi will have the [Mosquitto](http://mosquitto.org/) MQTT broker and [NodeRed](https://nodered.org/) installed on it