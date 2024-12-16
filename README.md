# Smartphone (Bluetooth) Controlled Car Using Arduino

## Project Overview
![Rover](https://private-user-images.githubusercontent.com/98210850/396102077-e174c69f-2b6a-47cd-bc56-40966fe708f1.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzQzNTM4NzgsIm5iZiI6MTczNDM1MzU3OCwicGF0aCI6Ii85ODIxMDg1MC8zOTYxMDIwNzctZTE3NGM2OWYtMmI2YS00N2NkLWJjNTYtNDA5NjZmZTcwOGYxLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDEyMTYlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMjE2VDEyNTI1OFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTZjNjdiZWQyMDc4YmE2ODIyOTA2NTYzMjEyN2ZlZDM0NzA5MGMwZjc2OWI3NTUyNzEwYjBhYWExOTU1ZTc5YmMmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.H_oEcVQyDVvK4ga-qFhiJlNZxVUaCpzfJf0wyowA5uI)

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
![Components](https://private-user-images.githubusercontent.com/98210850/396098981-6cc5555c-36da-4997-9b85-a21964a470c1.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzQzNTM0NjEsIm5iZiI6MTczNDM1MzE2MSwicGF0aCI6Ii85ODIxMDg1MC8zOTYwOTg5ODEtNmNjNTU1NWMtMzZkYS00OTk3LTliODUtYTIxOTY0YTQ3MGMxLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDEyMTYlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMjE2VDEyNDYwMVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTk2NGY1YzdlNDA1ODNlYzBkOTdhOTRjNGRhNTQ1ZTBkOTllOGU1ZmUxNDg0MTNmYmVlZDAxY2YwNmU1YzQ4NzkmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.DhP1FG7Br9xI6OHQdF3Bb7gIqMdfNNHgKz-u8S0hybs)

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
![Circuit Diagram](https://private-user-images.githubusercontent.com/98210850/396100544-ec095790-cbb5-4d48-9629-f547e3ac2e49.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzQzNTM1NzcsIm5iZiI6MTczNDM1MzI3NywicGF0aCI6Ii85ODIxMDg1MC8zOTYxMDA1NDQtZWMwOTU3OTAtY2JiNS00ZDQ4LTk2MjktZjU0N2UzYWMyZTQ5LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDEyMTYlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMjE2VDEyNDc1N1omWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPThkNTk5NzZjMDI0Yjc0NjQyNmY3MGQ0ZWNkYTkzOWMyZTYxMjAyOTRhNmE2MmY1NTdiMmI4NzQxNTM3YTUwZjYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.AmLbNKGjOtNd3GHo0lOmyPYYQS3pYs4IZNpV4wQhT9w)

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
![Arduino UNO](https://private-user-images.githubusercontent.com/98210850/396102563-af41251d-43ec-46a5-8e7e-c0b4005a1ebb.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzQzNTM5NzUsIm5iZiI6MTczNDM1MzY3NSwicGF0aCI6Ii85ODIxMDg1MC8zOTYxMDI1NjMtYWY0MTI1MWQtNDNlYy00NmE1LThlN2UtYzBiNDAwNWExZWJiLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDEyMTYlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMjE2VDEyNTQzNVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWM1ZTg2NGJiM2Y4NGRlOWMyZjVkOWU0MjhlYjcxOTAwNTAwZTIzOThlN2IzOGVjYTZkYjg0YTBkNGExYjI4NWYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.frhf82dE3Zbac40GFLvXPJgnnQBLanF64O2MSgIUfVw)

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
![Block Diagram](https://private-user-images.githubusercontent.com/98210850/396101483-94d19f5b-a511-45b4-be17-1da0ed350a59.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzQzNTM3NjMsIm5iZiI6MTczNDM1MzQ2MywicGF0aCI6Ii85ODIxMDg1MC8zOTYxMDE0ODMtOTRkMTlmNWItYTUxMS00NWI0LWJlMTctMWRhMGVkMzUwYTU5LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDEyMTYlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMjE2VDEyNTEwM1omWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTc4NGFiNjkyMjdlY2Y1NGIxYWRhMjJjOTkwZDY0MTRlMzE2MzYwZjUyNzY0ZmQ0NTQyYTExOTllNTQxOGNkNDQmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.B1zPNqmCPFTyUR446I3n27q08Ek-qkxenEM3uShmYeQ)

- **Bluetooth Module**: Connects the phone to the system.
- **Arduino UNO**: Processes received commands and controls motors.
- **DC Motor Driver**: Amplifies control signals for motor operation.
- **DC Motors**: Drives the car in desired directions.


