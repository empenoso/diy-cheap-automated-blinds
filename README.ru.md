# Автоматизация дешевых жалюзи ![GitHub](https://img.shields.io/github/license/empenoso/diy-cheap-automated-blinds) ![GitHub](https://img.shields.io/badge/labor%20hours-1%20day-orange)

Для этого проекта выбрал ESP8266 с прошивкой, которую можно добавить в Home Assistant за один клин. Без использования MQTT.

Read this in other languages: [English](README.md), [Русский язык](README.ru.md).

## Содержание
- [Материалы](https://github.com/empenoso/diy-cheap-automated-blinds#parts-top)
- [Прошивка ESPHome для ESP8266, которая управляет моторчиком в жалюзи](https://github.com/empenoso/diy-cheap-automated-blinds#esphome-firmware-top)
- [Правила для автоматизации закрытия жалюзи из Home Assistant](https://github.com/empenoso/diy-cheap-automated-blinds#automation-rule-for-home-assistant-top)
- [Фотографии](https://github.com/empenoso/diy-cheap-automated-blinds#photos-top)
- [Преимущества и недостатки](https://github.com/empenoso/diy-cheap-automated-blinds#advantages-and-disadvantages-of-project-top)

## Материалы [:top:](https://github.com/empenoso/diy-cheap-automated-blinds#diy-motorize--automate-blinds--)
1. [Леруа Мерлен жалюзи Inspire 100х160 см алюминий цвет белый](https://perm.leroymerlin.ru/product/zhalyuzi-inspire-100h160-sm-alyuminiy-cvet-belyy-16262144/) * 3 штуки

2. [Шаговый двигатель 28BYJ-48 5V 4 Phase DC Gear Stepper Motor + ULN2003 Driver Board](https://www.aliexpress.com/item/32896006818.html) * 3 штуки

3. [Плата LOLIN D1 mini V3.1.0 - WEMOS WIFI Internet of Things development board based ESP8266](https://www.aliexpress.com/item/32529101036.html) * 3 штуки

4. [Блок питания AC-DC 100-240V To 5V 2.5A Switching Power Supply Module](https://www.aliexpress.com/item/32898716031.html) * 1 штука

## Прошивка [ESPHome](https://esphome.io/components/stepper/index.html) для ESP8266, которая управляет моторчиком в жалюзи [:top:](https://github.com/empenoso/diy-cheap-automated-blinds#diy-motorize--automate-blinds--)
 
Я использую [дополнение для ESPHome Hass.io](https://github.com/esphome/hassio) для компиляции следующих файлов:
- [window_1.yaml](window_1.yaml)
- [window_2.yaml](window_2.yaml)
- [window_3.yaml](window_3.yaml)

![Home Assistant\ESPHome](ESPHome.png)

## Правила для автоматизации закрытия жалюзи из [Home Assistant](https://www.home-assistant.io/docs/automation/) [:top:](https://github.com/empenoso/diy-cheap-automated-blinds#diy-motorize--automate-blinds--)

При привышении определенного порога жалюзи [поворачиваются на 90 градусов](automations.yaml) и потом обратно соответственно.

![Home Assistant\Integrations](Home%20Assistant_integrations.png)

## Фотографии [:top:](https://github.com/empenoso/diy-cheap-automated-blinds#diy-motorize--automate-blinds--)
![Photos](/IMG_20191026_101014.jpg)
![Photos](/IMG_20191026_101100.jpg)
![Photos](/IMG_20191026_103251.jpg)

## Преимущества и недостатки [:top:](https://github.com/empenoso/diy-cheap-automated-blinds#diy-motorize--automate-blinds--)
+ Дешево.
- ESP8266 никогда не знает текущего положения жалюзи. Иногда, когда например вал прокручивается, приходится вручную подгонять под начальное положение нажатием кнопки в интерфейсе Home Assistant.
