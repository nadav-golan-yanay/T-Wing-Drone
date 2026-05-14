# T-Wing-Drone

**T-Wing** is a custom VTOL drone project I built as my final-year project in the Robotics program at Gvanim High School.  
The platform uses **three motors**, each mounted on a **servo-driven rotating mechanism**, combining multirotor control with custom mechanical design.

## Repository contents

This repository currently includes:

- `V22 full assembly 3D files/` — STL files for the full mechanical assembly
- `T-Wing_Params.params` — flight-controller parameter set
- `arducopter.apj` — ArduPilot firmware package used in this project

## Project highlights

- Custom airframe and wing/motor mounting system
- 3D-printed structural parts (PLA + ABS) with carbon-fiber reinforcements
- Iterative design based on real flight-test feedback
- Migration from early ESP32/Arduino prototypes to Pixhawk-based control

## Proof of success / flight tests

It took almost a year from the initial concept to the first successful takeoff.  
Flight tests are documented on my YouTube channel **NJGeek**:

- Channel: <https://www.youtube.com/channel/UCFTb9_tvUnTDQ8KEI29btOw>
- Playlist: <https://youtube.com/playlist?list=PLqjej9Hx4NUbdtqtBohuQlDSfjigC6vUl&si=ENThvdS27YvLaflj>

### First successful flight

My first successful flight was on **2023-05-19**:

- Video: <https://youtu.be/v9YFX8xqOcs>
- Clip asset:  
  <https://github.com/nadav-golan-yanay/T-Wing-Drone/assets/78790309/edb56a76-8f06-4417-a14c-41ca4fd376b4>

## Parts and 3D models

All model files are available in:

- [`V22 full assembly 3D files`](./V22%20full%20assembly%203D%20files)

Modeling and manufacturing workflow:

- CAD: [Onshape](https://www.onshape.com/en/)
- 3D printing: [FlashForge](https://flashforge.com/)

![TWing-Full-V22](https://github.com/nadav-golan-yanay/T-Wing-Drone/assets/78790309/63dcac5a-7471-424a-bd80-f48f89bf449f)

The assembly is built from four main modules: a body and three wings.  
Main material is PLA, with ABS used for heat-sensitive parts and carbon-fiber rods for reinforcement.

### Motor holder design notes

![Exploded_Motor_Holder](https://github.com/nadav-golan-yanay/T-Wing-Drone/assets/78790309/eb4dbcce-7ec2-4fd4-9dbd-57e81f796824)

The motor holder connects to a carbon-fiber bar using a clamp-based solution.  
During testing, motor heat caused PLA deformation, so the design evolved through several iterations:

1. ABS-only holder (rejected due to poor layer adhesion under load)
2. ABS spacers between motor and PLA base (improved, but not enough over time)
3. Additional thermal isolation layer between base and spacers (successful in long runs)

## Boards and controllers

The final version of the drone used a **Pixhawk 4 Mini** flight controller.

| Parameter | ESP32 | Arduino Uno | Pixhawk 4 Mini |
| :--- | :---: | :---: | :---: |
| Memory | 520 KB | 32 KB | 2 MB |
| Code stack | C++ | C++ | ArduPilot |
| Weight | 10 g | 25 g | 37.2 g |
| I/O voltage | 3.3 V | 5 V | 5 V |

### Why ESP32 and Arduino were used in early stages

The project started with ESP32 and Arduino due to budget limitations and available school hardware.  
That phase enabled rapid prototyping of:

- a custom radio system: <https://github.com/nadav-golan-yanay/com.git>
- motor/servo extension logic: <https://github.com/nadav-golan-yanay/Extender.git>
- custom PID experiments: <https://github.com/nadav-golan-yanay/PID.git>

This early work helped build system-level understanding before moving to Pixhawk + ArduPilot.

## Code and parameters

This repository includes the configuration artifacts used in the project:

- Parameters file: [`T-Wing_Params.params`](./T-Wing_Params.params)
- Firmware package: [`arducopter.apj`](./arducopter.apj)

> **Safety note:** Flight parameters and firmware should be reviewed and adapted for your frame, propulsion system, and local safety rules before use.

## Acknowledgments

I’m deeply grateful to everyone who helped make this project possible:

- Teachers and mentors, especially **Gal Arbel** and **Oded Valensi**
- My parents and family for continuous support
- **Efi Kastiel** and **Efix-Aviation** for equipment support and guidance
- Friends and students who helped with building, testing, filming, and reviews
- My classmates and project partners for technical and moral support

Thank you all for helping turn this idea into a flying system.
