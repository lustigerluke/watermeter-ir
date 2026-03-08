# watermeter-ir

## Description
Reading flowiq2200 watermeter via ir interface Kamst-IR Gateway and passing data via MQTT to homeassistant.

## Story
I recentrly purchased a [Kamst-IR Gateway](https://smartgateways.nl/en/make-your-kamstrup-multical-and-flowiq-meter-smart/) and found it somehow boring to have to find my way to get it to read my [flowiq2200](https://www.kamstrup.com/de-de/product-centre/flowiq-2200). This repository is meant to be my central place of knowledge and for sharing.

## HOW TO
### Assumtions
* Kamst-IR Gateway is connected to your WIFI
* Kamst-IR Gateway is showing some values via the REST-API
    * There is a link in the webUI to access the JSON content provided by the REST-API. Click it and make sure your there is a non-zero/non-empty volume reading.
* MQTT broker 
    * You can just install the homeassistant [MQTT-App](https://www.home-assistant.io/integrations/mqtt).

### What to do
1) Add the lines mentioned in *configuration.yaml* to your *configuration.yaml* file in hoeassistant root folder.
2) copy the *package* folder to your homeassistant root folder

## Optional: Discovery
See the README in *discovery* folder.


## HINTS

* **The ir-gateway has to be placed very precise.** 
  * There is a green and white led an the ir-gateway to indicate RX/TX communication. These leds are blinking while communicating with the flowiq2200 watermeter. 
    * If they are blinking synchronouse no data is received. 
    * If they are both flickering communication is established.
* The webUI of the ir-gateway is straigth forward. Do not enter any PREFIX if you are not sure about what you do.


