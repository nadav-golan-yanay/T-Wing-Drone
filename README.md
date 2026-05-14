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

## Original Hebrew project book

This project was originally documented as a full project book in Hebrew for the school robotics program.  
It includes the design process, engineering decisions, manufacturing notes, and flight-test development timeline behind T-Wing.
You can read it here:

<iframe src="https://docs.google.com/document/d/e/2PACX-1vRpgUPn3u3C4NKBrrm5369ePE8NgqHe6AcITnAAplzpBRE5xgx34mOA12HqonQQBGQqTkdLsOp1IHl_/pub?embedded=true"></iframe>

## Acknowledgments

I’m deeply grateful to everyone who helped make this project possible:

In this project, I received help from many people, whom I would like to thank. First and foremost, I would like to thank my subject teachers, [Gal Arbel](https://github.com/galarb) and [Oded Valensi](). Whether in modeling, programming, manufacturing, or writing the report, Gal and Oded were always by my side and supported me. Thank you for helping to push me to the limits of my abilities and beyond; under your guidance, even the sky is not the limit.

I want to extend my gratitude to my parents who supported me throughout the entire project and encouraged me to pursue this field. Thank you for every model airplane and drone you bought me, each one helped me gain the knowledge that enabled me to build this project. Many thanks to [Efi Kastiel](https://www.linkedin.com/search/results/all/?fetchDeterministicClustersOnly=true&heroEntityKey=urn%3Ali%3Afsd_profile%3AACoAADLQAJUBAUvj69bxqbnr-7TJYAfVfe6obSc&keywords=efi%20kastiel&origin=RICH_QUERY_SUGGESTION&position=0&searchId=0ba67cb9-c28c-4535-bafa-e0ef54953f92&sid=DP1&spellCorrectionEnabled=false) from [Efix-Aviation](https://www.linkedin.com/company/efixaviation/?originalSubdomain=il), who donated equipment and provided training regarding the drone. A big thank you to [Ariel Dubrovinski](), who guided me on how to use the Pixhawk controller and how to work with PID systems.

Thank you to the students from grades 9 and 7: [Tomer Ozer](https://github.com/TomerOzer), [Noam Ron](https://github.com/NoamRon1), [Yehav Kosi Friedman](https://github.com/yahavkosoi), [Dan Katzenellenbogen](https://github.com/Dan-Katzenellenbogen), [Yoav Aharoni](), [Neta Shen-Or](), [Hadas Rahman](), and [Yoav Paz](https://github.com/YoavPaz). Thank you for your help in building the project and supporting the code, whether it was just holding a part while I drilled or reviewing the code. You all helped greatly, and for that, I thank you.

A special thank you to [Roee Glotman](https://github.com/Roee-dev), my classmate, who was my partner at the beginning of the project. Many thanks to my fellow students in the subject: [Yotam Sharon](), [Daniel Shor](), [Dror Chen](), [Ori Zalgman](), [Daniel Semelik](https://github.com/DanielSmelik), [Yuval Rahman](), [Eran Salomon]() and [Raviv Klein](https://github.com/raviviviviv). Thank you very much for the help and support, for being with me during flight tests, for helping me film, and for letting me print before you so I could progress. Thank you very much to the school for the lab and project funding.

Finally, a huge thank you to my (ex)girlfriend, Daria Hebron. Thank you for your support and understanding. Thank you for every glass of water or toast you brought me in the late hours of the night when I was sitting at the computer working, thank you for letting me use your car to transport equipment, and thank you for all the emotional support you provided during all the difficulties.

Thank you all for helping turn this idea into a flying system.
