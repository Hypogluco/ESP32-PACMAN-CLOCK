# Pacman Clock with Weather Temperature and Color Customizations
"For the moment the code is in French, I will make a second version in English."

## Description
This project uses an ESP32 board and a 64x64 LED matrix display. While running a game demo in the background, the clock, date, and game map can be customized via a web page, allowing you to change colors and adjust brightness.

## Required Hardware
- **ESP32 30 Pin Board**
- **64x64 LED Matrix Display HUB75** (Compatible with the **ESP32-HUB75-MatrixPanel-I2S-DMA** library)

## Libraries Used
- **ESP32-HUB75-MatrixPanel-I2S-DMA**: for displaying on the LED matrix screen.
- **WiFiConnect**: for managing Wi-Fi connection.
- **CWDateTime**: for managing time and date.
- **HTTPClient**: for fetching weather data from the OpenWeatherMap API.
- **Preferences**: for managing the saving of settings (such as colors and brightness).
- **ezTime**: for handling time zones and synchronizing time.

## Features
- **Background Game Demo**: A Pacman game demo with ghosts runs in the background of the screen.
- **Automatic Brightness Adjustment**: The screen brightness is automatically adjusted based on the time to save energy.
- **Web Page Customization**: You can modify the colors of the clock, date, and game map.
- **Brightness Adjustment**: The screen brightness can be adjusted via the web page.
- **Settings Saving**: All settings, including colors and brightness, are saved even after a board restart.

## Notes
- The screen brightness is automatically adjusted based on the time to save energy.
- This project was created based on the GitHub projects "ClockWise" by jnthas and Otis Irachi.

## License
This project is under the MIT License, which means you are free to use, modify, and distribute it according to the license terms.

## Author
HypoGluco
November 2024

## Reminder for "ESP32-HUB75-MatrixPanel-I2S-DMA"
- **Modify the pins in the `"esp32-default-pins.hpp"` file for the 64x64 screen**. Without this modification, the screen will not work.
- Path to the pin configuration file: `C:\Users\*****\Documents\Arduino\libraries\ESP32_HUB75_LED_MATRIX_PANEL_DMA_Display\src\platforms\esp32\esp32-default-pins.hpp`

## Pin Configuration
Modify the `"esp32-default-pins.hpp"` file to define the pins used to connect the LED screen. Default configuration example:

```cpp
#pragma once

#define R1_PIN_DEFAULT  25
#define G1_PIN_DEFAULT  26
#define B1_PIN_DEFAULT  27
#define R2_PIN_DEFAULT  14
#define G2_PIN_DEFAULT  12
#define B2_PIN_DEFAULT  13

#define A_PIN_DEFAULT   23
#define B_PIN_DEFAULT   19
#define C_PIN_DEFAULT   5
#define D_PIN_DEFAULT   17
#define E_PIN_DEFAULT   18 // IMPORTANT: Change to a valid pin if using a 64x64px panel.

#define LAT_PIN_DEFAULT 4
#define OE_PIN_DEFAULT  15
#define CLK_PIN_DEFAULT 16


```

https://github.com/user-attachments/assets/bf49dcfc-0325-40cb-bc75-9e92f6833a43
