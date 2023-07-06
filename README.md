# Flex-Glove-Project

This Arduino project allows you to control servo motors with flex sensors, creating a glove that can mimic finger movements. By wearing the glove and flexing your fingers, you can control the movement of the servo motors.

## Table of Contents

- [Hardware Requirements](#hardware-requirements)
- [Wiring Convention](#wiring-convention)
- [Calibration](#calibration)
- [Setup](#setup)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Hardware Requirements

To build the Flex Glove Arduino project, you will need the following components:

- Arduino Lilypad
- 5 x Servo motors
- 5 x Flex sensors
- Jumper wires

## Wiring Convention

The flex sensors and servo motors are connected to the Arduino Lilypad according to the following wiring convention:

```
Finger  | Lilypad Pin
Thumb   | D5
Index   | D6
Middle  | D7
Ring    | D8
Pinky   | D9
```

## Calibration

Before using the Flex Glove, you need to calibrate the flex sensors. The calibration offsets for each finger are as follows:

```
Flex Sensor Range (Relaxed) | Flex Sensor Range (Contracted)
Thumb   | 260 - 330           | 400 - 500
Index   | 400 - 500           | 500 - 900
Middle  | 480 - 900           | 900 - 360
Ring    | 230 - 360           | 360 - 450
Pinky   | 380 - 450           | 450 - 500
```

These values will be used to map the flex sensor readings to servo motor angles.

## Setup

To set up the Flex Glove Arduino project, follow these steps:

1. Connect the servo motors and flex sensors to the Arduino Lilypad according to the wiring convention mentioned above.
2. Upload the code to the Arduino Lilypad.
3. Open the serial monitor with a baud rate of 9600.
4. Ensure that the flex sensors are in their relaxed position.
5. Note down the readings shown in the serial monitor for each finger.
6. Contract each finger and note down the new readings.
7. Update the `flexsensorRange` array in the code with the calibration offsets obtained from the previous step.
8. Save the changes and re-upload the code to the Arduino Lilypad.

## Usage

To use the Flex Glove Arduino project, follow these steps:

1. Wear the glove and ensure that the flex sensors are properly positioned on your fingers.
2. Power on the Arduino Lilypad.
3. Flex your fingers and observe the corresponding movements of the servo motors.
4. Adjust the calibration offsets if necessary to achieve the desired finger movements.
5. Have fun experimenting with different finger gestures and applications!

## Contributing

Contributions to the Flex Glove Arduino project are welcome. If you have any ideas, improvements, or bug fixes, feel free to open an issue or submit a pull request.
