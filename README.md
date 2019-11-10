# DIY Motorize & Automate Blinds ![GitHub](https://img.shields.io/github/license/empenoso/diy-cheap-automated-blinds)
Low price automation of blinds :electric_plug:. Blinds are also cheap.

I use ESP8266 with firmware that is native to Home Assistant. Without using MQTT.

## Table of contents
- [Parts](https://github.com/empenoso/diy-cheap-automated-blinds#parts)
- [ESPHome firmware](https://github.com/empenoso/diy-cheap-automated-blinds#esphome-firmware)
- [Automation rule for Home Assistant](https://github.com/empenoso/diy-cheap-automated-blinds#automation-rule-for-home-assistant)
- [Photos](https://github.com/empenoso/diy-cheap-automated-blinds#photos)
- [Advantages and Disadvantages of Project](https://github.com/empenoso/diy-cheap-automated-blinds#advantages-and-disadvantages-of-project)

## Parts
1. [Leroy Merlin Blinds Inspire 100x160 cm aluminum color white](https://perm.leroymerlin.ru/product/zhalyuzi-inspire-100h160-sm-alyuminiy-cvet-belyy-16262144/) * 3 pieces

2. [28BYJ-48 5V 4 Phase DC Gear Stepper Motor + ULN2003 Driver Board](https://www.aliexpress.com/item/32896006818.html) * 3 pieces

3. [LOLIN D1 mini V3.1.0 - WEMOS WIFI Internet of Things development board based ESP8266](https://www.aliexpress.com/item/32529101036.html) * 3 pieces

4. [AC-DC 100-240V To 5V 2.5A Switching Power Supply Module](https://www.aliexpress.com/item/32898716031.html) * 1 pieces

## [ESPHome](https://esphome.io/components/stepper/index.html) firmware
 
I am use [ESPHome Hass.io Add-On](https://github.com/esphome/hassio) to compile:
- [window_1.yaml](window_1.yaml)
- [window_2.yaml](window_2.yaml)
- [window_3.yaml](window_3.yaml)

![Home Assistant\ESPHome](ESPHome.png)

## Automation rule for [Home Assistant](https://www.home-assistant.io/docs/automation/)

Depending on the light level, the blinds [rotate 90 degrees.](automations.yaml)

![Home Assistant\Integrations](Home%20Assistant_integrations.png)

## Photos
![Photos](/IMG_20191026_101014.jpg)
![Photos](/IMG_20191026_101100.jpg)
![Photos](/IMG_20191026_103251.jpg)

## Advantages and Disadvantages of Project
+ Cheap.
- ESP8266 does not know the current position of the blinds. Sometimes you have to spin manually by command from the Home Assistant interface.
