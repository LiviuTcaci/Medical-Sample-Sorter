# Medical Sample Sorter

This repository contains the source code and documentation for the **Medical Sample Sorter**, a project developed for the Electronic Measurements and Sensors course at the Faculty of Automatic Control and Computers. The system uses an Arduino Uno and a TCS3200 color sensor to detect and differentiate medical samples based on their color. By mapping sensor readings to RGB values, the system classifies samples for sorting and further analysis.

## Overview

- **Purpose:**  
  To demonstrate how a TCS3200 color sensor can be integrated with an Arduino to perform precise color detection for sorting and differentiating medical samples.

- **Key Features:**  
  - **Color Detection:** Reads red, green, and blue pulse widths from the TCS3200 sensor.
  - **Data Mapping:** Maps raw sensor data to a 0–255 scale for each color channel.
  - **Serial Output:** Prints the computed RGB values to the Serial Monitor for real-time monitoring and debugging.
  - **Alternate Hardware Options:**  
    In addition to using the TCS3200, the system can also be implemented with a setup that includes:
    - ISL29125 Color Sensor
    - Two-channel logic converter
    - 4 LEDs
    - 4 Resistors

## Hardware & Software

- **Hardware:**  
  - Arduino Uno  
  - TCS3200 Color Sensor *or* an alternative configuration (ISL29125, two-channel logic converter, 4 LEDs, 4 Resistors)  
  - Connecting wires and a suitable power supply

- **Software:**  
  - Arduino IDE for coding and uploading the sketch  
  - C/C++ language (Arduino sketch) for sensor interfacing and data processing

## How It Works

1. **Sensor Configuration:**  
   The TCS3200 sensor is set up with its frequency scaling pins (S0–S3) configured to output a 20% scaled signal.

2. **Color Measurement:**  
   Separate functions are used to measure the pulse width corresponding to red, green, and blue channels. These pulse widths are then mapped to RGB values (0–255).

3. **Output:**  
   The computed RGB values are output to the Serial Monitor, which can be used to verify the sensor’s performance and the accuracy of the color detection algorithm.

## Getting Started

1. **Hardware Setup:**  
   - Connect the TCS3200 sensor (or the alternative sensor configuration) to the Arduino Uno using the defined pins in the sketch.
   - Ensure proper power supply and sensor orientation for accurate detection.

2. **Software Setup:**  
   - Open the provided `main.ino` file in the Arduino IDE.
   - Verify or adjust the calibration values (`redMin`, `greenMin`, `blueMin`, etc.) if necessary.

3. **Upload and Run:**  
   - Upload the sketch to your Arduino Uno.
   - Open the Serial Monitor (set to 9600 baud) to observe the RGB values detected by the sensor in real time.

## Results & Conclusions

The system has been successfully implemented to detect subtle differences in color, proving its potential for sorting medical samples based on color. The project demonstrates how low-cost sensor technology can be applied in the medical field to enhance diagnostic and sorting procedures.
