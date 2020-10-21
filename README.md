English | [简体中文](./README_zh-CN.md)

# Xiaomi Mijia BLE Temperature Hygrometer 2

[![GitHub Release][releases-shield]][releases]

This is a custom component for home assistant to integrate the Xiaomi Mijia BLE Temperature Hygrometer 2 (LYWSD03MMC).

![LYWSD03MMC](/pictures/LYWSD03MMC.jpg)
![LYWSDCGQ/01ZM](/pictures/LYWSDCGQ01ZM.jpg)

## Supported devices

| Name                   | Model                  | Model no. |
| ---------------------- | ---------------------- | --------- |
| Xiaomi Mijia BLE Temperature Hygrometer  |  | LYWSDCGQ/01ZM |
| Xiaomi Mijia BLE Temperature Hygrometer 2  |  | LYWSD03MMC  |

## Features

### Mijia BLE Temperature Hygrometer 2 (LYWSD03MMC)

- Attributes
  - `temperature`
  - `humidity`
  - `battery`

## Install

You can install this custom component by adding this repository ([https://github.com/leonxi/mitemp_bt2](https://github.com/leonxi/mitemp_bt2/)) to [HACS](https://hacs.xyz/) in the settings menu of HACS first. You will find the custom component in the integration menu afterwards, look for 'Xiaomi Mijia BLE Temperature Hygrometer 2 Integration'. Alternatively, you can install it manually by copying the custom_component folder to your Home Assistant configuration folder.


## Setup

```yaml
# configuration.yaml

sensor:
  - platform: mitemp_bt2
    mac: 'A4:C1:38:AA:AA:AA'
    mode: 'LYWSD03MMC'
    name: book room
    period: 60
  - platform: mitemp_bt2
    mac: 'A4:C1:38:FF:FF:FF'
    mode: 'LYWSD03MMC'
    name: living room
    period: 60
```

Configuration variables:
- **mac** (*Required*): The MAC of your device.
- **mode** (*Optional*): The mode of your device. Default LYWSD03MMC
- **name** (*Optional*): The name of your device.
- **period** (*Optional*): The scan period of your device. Default 300 seconds.

## Panel Sample

  ![LYWSD03MMC_PANEL_SHOW](/pictures/sample_panel_1.png)
