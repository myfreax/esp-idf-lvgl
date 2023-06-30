# ESP-IDF LVGL Template

It Can Start LVGL Project with ESP-IDF Framework For you

## Get Start

```
git clone --recurse-submodules git@github.com:myfreax/esp-idf-lvgl.git
idf.py build
```

## Configure Screen Display Size

You need to set the display horizontal and vertical size, color depth and swap of RGB565 color on the LVGL configuration menuconfig (it's not handled automatically)

```
idf.py menuconfig
```

`Component config` → `LVGL ESP Drivers` → `LVGL TFT Display controller`

- Maximal horizontal resolution
- Maximal vertical resolution

## Tested ESP-IDF Versions:

- master (5.2)
- release/v5.1
- release/v5.0
- release/v4.4
- release/v4.3
- release/v4.2

## Tested LVGL Versions

- release/v8.3

## Tested MCUs

- ESP32-WROVER-E (Freenove, 240Mhz, 4MB Flash, 8MB PSRAM)
- ESP32-S3-WROOM-1 [N8R8] (Freenove, 240Mhz, 8MB Flash, 8MB PSRAM)

## Tested Displays

- 128x64 SSD1306 OLED
- 128x128 ST7735
- 320x240 ILI9341 (with HR2046)
- 240x240 GC9A01 (round display)
- 170×320 ST7789V2
- 320x480 ILI9486 (with XPT2046)

## Additional Changes

- change touch controller readouts to verbose logger
- use spi dma chan auto for esp32s3
- fixes for 128x128 ST7735 display

## Thank

[hiruna/lvgl_esp32_drivers](https://github.com/hiruna/lvgl_esp32_drivers/tree/develop/lvgl_8.3.7_idf_5.2)
