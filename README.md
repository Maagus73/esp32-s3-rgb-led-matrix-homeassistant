# waveshare-esp32-s3-rgb-led-matrix Home Assistant Integration

[🃆 Waveshare - ESP32-S3 RGB LED Matrix Board](https://www.waveshare.com/esp32-s3-matrix.htm?srsltid=AfmBOooSF-I5TuIkvmns72VO76DECQ94LocaBvKIVIYyzNIn6dSMUuu1)

A ready-made configuration that can be easily integrated with ESPHome (2026.7.4) & Home Assistant (2026.8.1).

\*\* Please note that this is a German-language project and all texts in the configurations and templates are in German. However, these can easily be changed in the single YAML file.

## ⭐ Features

<img src="docs/images/features.png"/></br>

Matrix automatic rotation: Checks if the matrix is ​​upside down and adjusts the scrolling text accordingly (including the matrix effect).  
Matrix Color: Change the color of scrolling text or other color changes in the effects.</br>
Matrix Speed: Well, that should be clear.</br>
Matrix Brightness: Well, that should be clear.</br>
Matrix Scrolling text: Well, that should be clear.</br>
Matrix Modus: This section presents the available display options.</br>

- Specifically: OFF turns off all LEDs. Try out all the others to see if you like them.
- All effects can be adjusted to their default brightness directly in the YAML file, so you don't need to change them via the matrix brightness.
- All effects were created with the kind support of ChatGPT, and no ESPHome standard effect is used.

## 📦 Installation

I assume that ESPHome (ESPHome Builder) is familiar and, of course, already installed. Otherwise, there is a wealth of information available via search engines regarding ESPHome and Home Assistant.

1. copy the yaml file and the folder to your esphome folder:

   <img src="docs/images/folder.png"/>

2. change inside \*.yaml file the mentioned blocks to your needs... or what is provided to you after initial

```yaml
substitutions:
  name: esp32-s3-matrix # Adjust accordingly
  friendly_name: "ESP32 S3 Matrix" # Adjust accordingly

api:
   encryption:
   key: "key" # Adjust accordingly

ota:

- platform: esphome
  password: "password" # Adjust accordingly

wifi:
ssid: !secret wifi_ssid
password: !secret wifi_password

ap:
ssid: "ESP32-S3-Matrix" # Adjust accordingly
password: "password" # Adjust accordingly
```

3. After you've made your adjustments, plug it in and flash it using ESPHome Builder </br>(if not already done in ESPHome Builder because of your adjustments above).
4. Now go to Settings - Devices & Services and click + Add Integration at the bottom. or you do it directly inside the ESPHome Bulder if you like

5. you should see your device now in devices on your Home Assistant

## This was all compiled for a colleague and will not be maintained or supported further. You can use it if you like or not.</br></br>
