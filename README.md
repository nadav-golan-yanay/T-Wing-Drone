# T-Wing-Drone
*T-Wing* is a drone that I built in my final year in the Robotics program at Gvanim High School. The drone has three motors, each on a different servo that rotates the motor.

 **image**

## Thanks To
In this project, I received help from many people, whom I would like to thank. First and foremost, I would like to thank my subject teachers, [Gal Arbel](https://github.com/galarb) and [Oded Valensi](). Whether in modeling, programming, manufacturing, or writing the report, Gal and Oded were always by my side and supported me. Thank you for helping to push me to the limits of my abilities and beyond; under your guidance, even the sky is not the limit.

I want to extend my gratitude to my parents who supported me throughout the entire project and encouraged me to pursue this field. Thank you for every model airplane and drone you bought me, each one helped me gain the knowledge that enabled me to build this project. Many thanks to [Efi Kastiel](https://www.linkedin.com/search/results/all/?fetchDeterministicClustersOnly=true&heroEntityKey=urn%3Ali%3Afsd_profile%3AACoAADLQAJUBAUvj69bxqbnr-7TJYAfVfe6obSc&keywords=efi%20kastiel&origin=RICH_QUERY_SUGGESTION&position=0&searchId=0ba67cb9-c28c-4535-bafa-e0ef54953f92&sid=DP1&spellCorrectionEnabled=false) from [Efix-Aviation](https://www.linkedin.com/company/efixaviation/?originalSubdomain=il), who donated equipment and provided training regarding the drone. A big thank you to [Ariel Dubrovinski](), who guided me on how to use the Pixhawk controller and how to work with PID systems.

Thank you to the students from grades 9 and 7: [Tomer Ozer](https://github.com/TomerOzer), [Noam Ron](https://github.com/NoamRon1), [Yehav Kosi Friedman](https://github.com/yahavkosoi), [Dan Katzenellenbogen](https://github.com/Dan-Katzenellenbogen), [Yoav Aharoni](), [Neta Shen-Or](), [Hadas Rahman](), and [Yoav Paz](https://github.com/YoavPaz). Thank you for your help in building the project and supporting the code, whether it was just holding a part while I drilled or reviewing the code. You all helped greatly, and for that, I thank you.

A special thank you to [Roee Glotman](https://github.com/Roee-dev), my classmate, who was my partner at the beginning of the project. Many thanks to my fellow students in the subject: [Yotam Sharon](), [Daniel Shor](), [Dror Chen](), [Ori Zalgman](), [Daniel Semelik](https://github.com/DanielSmelik), [Yuval Rahman](), [Eran Salomon]() and [Raviv Klein](https://github.com/raviviviviv). Thank you very much for the help and support, for being with me during flight tests, for helping me film, and for letting me print before you so I could progress. Thank you very much to the school for the lab and project funding.

Finally, a huge thank you to my girlfriend, Daria Hebron. Thank you for your support and understanding. Thank you for every glass of water or toast you brought me in the late hours of the night when I was sitting at the computer working, thank you for letting me use your car to transport equipment, and thank you for all the emotional support you provided during all the difficulties.

## Proof of success / Flight tests
It took almost a year from when I first thought about the drone concept until I managed to take off with it. I've uploaded all of my flight tests to my YouTube channel [NJGeek](https://www.youtube.com/channel/UCFTb9_tvUnTDQ8KEI29btOw). You can see them all in the playlist [T-Wing Flight test](https://youtube.com/playlist?list=PLqjej9Hx4NUbdtqtBohuQlDSfjigC6vUl&si=ENThvdS27YvLaflj). Enjoy.

### Successful Flights
I define a successful flight as a flight that the drone tookoff, landed and wasn't demaged.
#### First Flight
My First successful flight was in May 19th 2023, you can see it in this video [ניסויי טיסה - 19.05.2024 - Flight Test
](https://youtu.be/v9YFX8xqOcs). Here you can see a small part from the video:

https://github.com/nadav-golan-yanay/T-Wing-Drone/assets/78790309/edb56a76-8f06-4417-a14c-41ca4fd376b4

My conclusion from the first flight were:
- bla bla bla I need to finish this----------------------------------------------------------------------------------


#### Secound Flight
After my first flight draw conclusions,



## Parts and 3D models
You can see all of the models in the [3D models folder](https://github.com/nadav-golan-yanay/T-Wing-Drone/tree/0b038b9dfee622c4904f3aa1510728cdbde3ab1c/V22%20full%20assembly%203D%20files).
I used [onshape](https://www.onshape.com/en/) for the 3D modeling and [FlashForge Printers](https://flashforge.com/) for the 3D printing.

![TWing-Full-V22](https://github.com/nadav-golan-yanay/T-Wing-Drone/assets/78790309/63dcac5a-7471-424a-bd80-f48f89bf449f)
This image shows the full assembly of the drone. The drone is built from four main parts: the body and three wings. I used PLA filament as my main material; some parts are 3D printed from ABS filament, and there are a few carbon fiber bars that connect all the parts together. At the end of each wing, you can see big circles. These indicate the length of the drone propellers, showing where the propellers would be.

### Motor holder
![Exploded_Motor_Holder](https://github.com/nadav-golan-yanay/T-Wing-Drone/assets/78790309/eb4dbcce-7ec2-4fd4-9dbd-57e81f796824)

The motor holder is connected to the wing with a carbon fiber bar. At first, I tried to drill a hole in the bar, but it broke. In this version of the drone, the motor holder connects to the bar with a clamp. I wrapped the carbon fiber with electrical tape to reduce the sliding of the motor holder. This method worked better than I expected. The PLA is flexible and strong enough that it doesn't break, and it holds the motor in place.

The motor holder is built from three different parts. The blue part in the image is the main part; it's the base of the motor holder and is 3D printed from PLA filament. The black parts are the clamps that secure the motor holder in place, also printed from PLA filament. The white parts are spacers between the motor and the motor holder, printed from ABS filament.

In one of the first flight tests, I discovered that the motor heats up to a point where the PLA under it melts. My first solution was to print the motor holder from ABS filament, but I learned that its layer adhesion isn't good, and the part broke when I started the motors. The second solution I tried was to add spacers (the blue parts) between the PLA and the motor. The spacers are 3D printed from ABS filament, which is more resistant to heat than PLA. This solution worked at first, but over time, the PLA melted under the ABS. The third solution came from my teacher, Oded Valensi. He suggested adding parchment paper between the base (blue part) and the spacers (white parts) to further isolate the heat. This worked, and I managed to run the motors for a long time.

### Servo Arm Adaptor
**image**

To connect the servo to the carbon fiber bar that the motor is siting on I crated an adaptor. The desgin of the adaptor is uniq becouse it uses a spacial fitcher of 3D printing - the printer stops the printing in a cirtin layer, the servo arm is insert to it and than the printings is continue.

I used the adventure 3 printer becouse of it's grate accuracy, even when I touched the printer platform when I incert the servo arm I didn't demaged the printing quality. I used the **Flashforge** slicer, here is the function in the slicer **to be continued**


## Borad and Microcontrollers

In my last version of the drone I used the pixhawk 4 mini flight controller (link).
In here you can see a tabel of all of the borada and microcontrollers that I used:

ESP32 | Arduino uno | Archer 6 | PH4 mini
