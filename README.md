# Medical Sample Sorting and Differentiation System
A color-based medical sample classification system using Arduino and TCS3200 color sensor.

## Overview

This project implements an automated system for sorting and differentiating medical samples based on their color profiles. By utilizing precise color detection technology, the system can categorize samples with higher accuracy and efficiency than manual sorting methods.

## Features

- Real-time RGB color detection
- Custom calibration for laboratory environment
- Digital color mapping (0-255 scale)
- Serial output for monitoring

## Hardware Components

- Arduino Uno microcontroller
- TCS3200 Color Sensor module
- Connecting wires
- Optional: Sample holding/feeding mechanism

## Pin Configuration

| TCS3200 Pin | Arduino Pin |
|-------------|-------------|
| S0          | 4           |
| S1          | 5           |
| S2          | 6           |
| S3          | 7           |
| OUT         | 8           |
| VCC         | 5V          |
| GND         | GND         |

## Software Requirements

- Arduino IDE
- Serial Monitor (included in Arduino IDE)

## Installation and Setup

1. Connect the TCS3200 sensor to the Arduino according to the pin configuration table
2. Install Arduino IDE if not already installed
3. Download the project code
4. Open the `.ino` file in Arduino IDE
5. Upload the code to your Arduino board

## Calibration

The system relies on proper calibration for accurate color detection. The current code includes default calibration values:

```
int redMin = 52;    int redMax = 241;
int greenMin = 89;  int greenMax = 275;
int blueMin = 85;   int blueMax = 199;
```

For optimal performance in your specific environment:
1. Use the included calibration sketch (not shown in current files)
2. Update the min/max values in the main code

## Usage

1. Position the sensor at an appropriate distance from sample (typically 1-2cm)
2. Ensure consistent lighting conditions
3. Run the system and monitor RGB values via Serial Monitor
4. Implement sorting logic based on color profiles of your specific samples

## Output

The system outputs RGB values (0-255 scale) to the Serial Monitor in the format:
```
Red = [value] - Green = [value] - Blue = [value]
```

## Applications

- Clinical laboratory sample sorting
- Medical test result differentiation
- Quality control for reagents and solutions
- Automated medical diagnostics

## Future Improvements

- Add physical sorting mechanism
- Implement machine learning for improved classification
- Create a database of sample color profiles
- Add a display interface for visual feedback
- Integrate with laboratory information systems

## References

- [TCS3200 Color Sensor Datasheet](https://www.mouser.com/catalog/specsheets/tcs3200-e11.pdf)
- [Arduino Official Documentation](https://www.arduino.cc/)
- [DroneBot Workshop Color Sensing Tutorial](https://dronebotworkshop.com/arduino-color-sense/)
