# Smartphone (Bluetooth) Controlled Car Using Arduino

## Project Overview
This project demonstrates how to control a car using a smartphone via Bluetooth. The car's operations are managed by an Arduino UNO microcontroller, Bluetooth module HC-05, and a motor driver, making it a simple and efficient system for controlling movement in various directions. The primary focus is on using easily accessible hardware and software to achieve precise control.

---

## Abstract
This project employs Arduino, a motor driver, and a Bluetooth module to create a Bluetooth-controlled car. It replaces traditional microcontrollers and IR sensors with the Arduino platform and a Bluetooth module. Users can operate the car using any Android or iOS device, making it an accessible and versatile solution.

---

## Features
- Bluetooth-based communication for remote control.
- Compatibility with Android devices.
- Wide control range with no physical barriers affecting performance.
- Easily replaceable remotes with any Android device.

---

## Components Required
![Components](path/to/components_image.jpg)

- **Arduino UNO**: The brain of the system, which processes the control commands.
- **Motor Driver L293D**: Amplifies the Arduino's control signals to power the motors.
- **Bluetooth Module HC-05**: Enables communication between the Arduino and the smartphone.
- **Two DC Motors**: Control the car's movement.
- **Robot Car Chassis**: Provides the physical frame for the car.
- **Jumper Wires**: Connect components.
- **Breadboard**: Facilitates prototyping.
- **9V Battery**: Powers the system.

---

## Circuit Description
![Circuit Diagram](path/to/circuit_diagram_image.jpg)

1. **Power Supply**: Rechargeable batteries are used for the Arduino and motor driver.
2. **Bluetooth Pairing**: The phone connects to the HC-05 module with a default pairing password of `1234`.
3. **Control Application**: Use the "CAR BLUETOOTH RC" app (available on Google Play Store).
4. **Command Processing**: Arduino processes commands like "F" for forward, "B" for backward, etc., to control motor movement.
5. **Motor Control**: Digital pins 10-13 of Arduino connect to the motor driver's inputs to control two DC motors.

---

## Operations
![Operation Block Diagram](path/to/operation_block_diagram_image.jpg)

The car supports the following movements:
- **Forward**: Command `F`
- **Backward**: Command `B`
- **Stop**: Command `S`
- **Turn Right**: Command `R`
- **Turn Left**: Command `L`
- **Forward Right**: Command `I`
- **Backward Right**: Command `J`
- **Forward Left**: Command `G`
- **Backward Left**: Command `H`

---

## Advantages of Arduino
![Arduino UNO](path/to/arduino_uno_image.jpg)

- Open-source and beginner-friendly.
- Compatible with multiple operating systems (Windows, macOS, Linux).
- Easily programmable and reconfigurable.
- Extensive support for add-on shields like Bluetooth and motor shields.

---

## Usage Instructions
1. Assemble the components as per the circuit diagram.
2. Install the "CAR BLUETOOTH RC" app on your Android device.
3. Pair your smartphone with the HC-05 Bluetooth module using the password `1234`.
4. Open the app and connect to the car.
5. Use the app's interface to control the car's movement.

---

## Block Diagram
![Block Diagram](path/to/block_diagram_image.jpg)

- **Bluetooth Module**: Connects the phone to the system.
- **Arduino UNO**: Processes received commands and controls motors.
- **DC Motor Driver**: Amplifies control signals for motor operation.
- **DC Motors**: Drives the car in desired directions.

---

## References
- Ujjwal Kumar, Deepak Rasaily, Priyanka Rana. "Cell phone-Based Device Control with Voice Acknowledgment", International Journal of Engineering Trends and Technology (IJETT).
- HACKSTER.IO
- Google and WikiHow

---

### Replace the image placeholders (e.g., `path/to/components_image.jpg`) with the actual file paths in your repository or URLs of the images.

Save this file as `README.md` in the root directory of your GitHub repository for it to appear on the main project page.
