---
title: "RGB LED Controller ESPHome"
weight: 3
---


## Table of content
<!-- TOC tocDepth:2..3 chapterDepth:2..6 -->

- [Table of content](#table-of-content)
- [Introduction](#introduction)
  - [Idee](#idee)
    - [Wiring](#wiring)
    - [ESPHome](#esphome)
    - [Image Files](#image-files)
- [Datasheets](#datasheets)
  - [ESP8266](#esp8266)
  - [IRLZ14N](#irlz14n)

<!-- /TOC -->


## Introduction

{{% notice style="green" title="Info" icon="fa-solid fa-circle-info" %}}
Project is Done!
{{% /notice %}}

A 12V simple RGB controller with ESPHome support.

### Idee
This project uses an ESP8266 microcontroller to control 12V LED strips (RGB) using PWM (Pulse Width Modulation) via MOSFETs, and is configured through ESPHome for seamless integration with Home Assistant.

#### Wiring
Connect the 12V+ from the power supply to the + input of the LED strip. The – (negative) from the strip goes to the Drain of an N-channel MOSFET. Connect the Source of the MOSFET to GND, shared with both the ESP and power supply. The Gate is driven by a GPIO pin. Ensure the ESP GND and power supply GND are connected. The ESP8266 is supplied using a DC to DC buck converter with the output Voltage set to 3.3V the input is connected directly to the 12V supply Voltage.

#### ESPHome
```yaml
esphome:
  name: georg-leds-rgb
  friendly_name: Georg LEDs RGB

esp8266:
  board: esp01_1m

# Enable logging
logger:

captive_portal:
  
# Example configuration entry
output:
  - platform: esp8266_pwm
    pin: 13
    id: output_component1
  - platform: esp8266_pwm
    pin: 12
    id: output_component2
  - platform: esp8266_pwm
    pin: 14
    id: output_component3


# Example configuration entry
light:
  - platform: rgb
    name: "Living Room Lights"
    red: output_component1
    green: output_component2
    blue: output_component3

# Enable Home Assistant API
api:
  encryption:
    key: "key"

ota:
  - platform: esphome
    password: "psw"

wifi:
  ssid: !secret wifi_ssid
  password: !secret wifi_password

  # Enable fallback hotspot (captive portal) in case wifi connection fails
  ap:
    ssid: "Georg-Leds-Rgb Fallback Hotspot"
    password: "psw"

```

#### Image Files
![](img/WhatsApp%20Image%202025-05-04%20at%2010.53.32.jpeg)

## Datasheets
### ESP8266
{{% button href="https://www.studiopieters.nl/esp8266-pinout/" style="accent" icon="download" iconposition="right" %}}Get Pinout for ESP8266{{% /button %}}

### IRLZ14N
{{% button href="https://www.vishay.com/docs/91289/irfz14.pdf" style="red" icon="download" iconposition="right" %}}Get Datasheet for N-MOSFET{{% /button %}}
