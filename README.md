# Custom Quadcopter Flight Controller

An experimental quadcopter flight controller developed from scratch using a Teensy 4.0 microcontroller and an MPU6050 inertial measurement unit (IMU). The project explores embedded programming, sensor data processing, PID control, and custom PCB design for drone flight stabilization.

## Project Overview

The goal of this project is to design and develop a custom flight controller rather than rely on a commercially available flight controller.

The project covers hardware design, firmware development, sensor integration, receiver input processing, motor control, and flight testing.

This is an ongoing engineering project, with improvements made through experimentation and testing.

## Features

- Custom flight controller based on the Teensy 4.0.
- Sensor data integration.
- IMU data processing for attitude estimation.
- Altittude estimation using Barometer measurements.
- PID-based flight stabilization.
- RC receiver input using a FlySky FS-iA6B receiver in PPM mode.
- ESC signal generation for four brushless motors.
- Custom circuit and PCB design using EasyEDA.

*Feature status may change as development progresses.*

## Hardware Components

| Component | Purpose |
|---|---|
| Teensy 4.0 | Main flight controller |
| MPU6050 | Acceleration and angular velocity measurements |
| FlySky FS-iA6B | RC receiver |
| Brushless motors | Quadcopter propulsion |
| Electronic Speed Controllers (ESCs) | Brushless motor control |
| LiPo battery | Main power source |
| Custom PCB | Flight controller electronics |
| BME280 | Atomospheric pressure measurements |

## Software and Tools

- **Programming:** Arduino-compatible C++
- **Microcontroller:** Teensy 4.0
- **PCB design:** EasyEDA
- **Sensor interface:** I²C
- **Control system:** PID control

## Repository Structure

The repository may contain the following files and folders as the project develops:

- `firmware/` — Flight controller source code.
- `hardware/` — Circuit diagrams and PCB design files.
- `docs/` — Design notes, wiring diagrams, and technical documentation.
- `README.md` — Project overview and documentation.


## How It Works

The MPU6050 measures the quadcopter's acceleration and angular velocity while the Barometer measures the atmospheric pressure. The Teensy processes these measurements to estimate the craft's attitude and calculate stabilization corrections.

RC commands from the receiver provide pilot control inputs. The control algorithm combines these inputs with the estimated attitude or angular rates to determine motor commands.

The ESCs receive control signals from the Teensy and regulate the speeds of the four brushless motors.

## Current Development Status

This project is under active development. Work includes sensor integration, receiver input handling, motor control, PID tuning, and flight testing.

Future improvements may include better sensor filtering, more reliable stabilization, improved PCB layout, and additional flight-control features.

## Safety Notice

This project is experimental. Incorrect wiring, unstable control parameters, or hardware failures can cause unexpected motor operation and crashes.

Remove all propellers during initial electronics testing, verify motor order and rotation direction, and test the control system carefully before attempting flight.

## Contributions and Feedback

Suggestions, bug reports, and technical feedback are welcome. If you are interested in embedded systems, flight control, or DIY drone development, feel free to explore the project.

## License

This project is licensed under the terms of the license specified in the LICENSE file.
