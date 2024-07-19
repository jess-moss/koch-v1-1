# Alexander Koch Arm V1.1

This folder the instructions to assembly a slightly modified version of the [Alexander Koch Arms](https://github.com/AlexanderKoch-Koch/low_cost_robot). 

## Assembly Instructions

### Leader Arm

| Part | Amount | Unit Cost (US) | Buy US | Unit Cost (EU) | Buy EU | Unit Cost (UK) | Buy UK |
|---|---|---|---|---|---|---|---|
| Dynamixel XL330-M077-T | 6 | $24 | [Robotis](https://www.robotis.us/dynamixel-xl330-m077-t) | 40-46€ | [MyBotShop](https://www.mybotshop.de/DYNAMIXEL-XL330-M077-T)-[GenRobots](https://www.generationrobots.com/en/403818-dynamixel-xl330-m077-t-servo-motor.html) | £27 | [RoboSavvy](https://robosavvy.co.uk/robotis-dynamixel-xl330-m077-t.html) |
| XL330 Frame and Idler Wheel 4pcs set | 1 | $10 | [Robotis](https://www.robotis.us/fpx330-h101-4pcs-set) | 12€ | [GenRobots](https://www.generationrobots.com/en/403860-FPX330-H101-hinge-frame-and-idler-set-dynamixel-xl330.html) | £10 |  [RoboSavvy](https://robosavvy.co.uk/fpx330-h101-4pcs-set.html) |
| Waveshare Serial Bus Servo Driver Board | 1 | $10 | [Amazon](https://a.co/d/7C3RUYU) | 6€ | [GenRobots](https://eckstein-shop.de/WaveShare-Serial-Bus-Servo-Driver-Board-for-ST-SC-Serial-Bus-Servos-EN) | £8 | [Amazon](https://www.amazon.com/Waveshare-Integrates-Control-Circuit-Supports/dp/B0CTMM4LWK/) |
| 5V Power Supply | 1 | $6 | [Amazon](https://a.co/d/5u90NVp) | 9€ | [Amazon](https://www.amazon.fr/LEYF-Alimentation-Universelle-Adaptateur-Enfichable/dp/B09NGVWBSY) | £4 | [Amazon](https://a.co/d/5u90NVp)|
| Jumper Wires 3*40 pcs set (M-M, M-F, F-F) | 1 | $7 | [Amazon](https://a.co/d/hQfk2cb) | 9€ | [Amazon](https://www.amazon.fr/AZDelivery-Jumper-Cavalier-C%C3%A2ble-Arduino/dp/B074P726ZR) | £5 | [Amazon](https://a.co/d/hQfk2cb)|
| Table Clamp | 1 | $6 | [Amazon](https://a.co/d/4KEiYdV) | n/a | n/a | £5 | [Amazon](https://a.co/d/4KEiYdV) |
| Table Clamp 4pcs set | 1 | n/a | n/a | 14€ | [Amazon](https://www.amazon.fr/CAUTIOUS-Serre-Joint-R%C3%A9glable-Serre-Joints/dp/B0CJMB3SKH) | n/a | n/a |
| 1.5mm Star/Cruciform Screwdriver 2pcs set | 1 | n/a | n/a | 7€ | [Amazon](https://www.amazon.fr/sourcing-map-Cruciforme-%C3%89lectroniques-R%C3%A9paration/dp/B0BQ69J2QF) | n/a | n/a |
| 1.5mm Star/Cruciform Screwdriver included in set | 1 | $6 | [Amazon](https://www.amazon.com/Choice-9-Piece-Precision-Screwdriver-Phillips/dp/B0747DYJJR) | n/a | n/a | £5 | [Amazon](https://www.amazon.com/Choice-9-Piece-Precision-Screwdriver-Phillips/dp/B0747DYJJR)
| Total | | $189 | | 297€ | | £199 | |

Video of the Assembly: [GoogleDrive](https://drive.google.com/file/d/175ARhMbZ5WLxKjbbCx7fIGH7QuZW5ajk/view?usp=drive_link) #TODO: Update with Youtube Video later.

1. Order all off the shelf parts from the BILL_OF_MATERIALS.md.
2. Print all parts with a 3D printer.
   1. The STL files are in `hardware/leader/STL`
   2. Precision: 0.2mm minimum height layer
   3. Material: PLA, ABS, PETG or other reasonably strong plastics.
   4. Suggested: Prusa Mini+, Bambu P1, Ender3, etc.
3.  Scan each motor.
    1.  Connect the driver board to a computer (should work with Linux and MacOS)
    2.  Figure out the device name (e.g. tty.usbmodem57380045631 for MacOS): ```ls /dev/tty.*```
    3.  Scan each motor individually with [Dynamixel Wizard](https://emanual.robotis.com/docs/en/software/dynamixel/dynamixel_wizard2/)
        1. Set the baudrate to 1M for all motors
        2. Set the servo IDs to 1 for the shoulder to 5 (6 if using the elbow-to-wrist extension) for the gripper servo
4.  Follower the video to in assembling the mechanical structure.
5.  Use the electrical diagram to wire the robot
    1.  Using 6 Dynamixel motor cables, daisy chain each motor to the one after it. Tip: Each Dynamixel has two ports, but they are electrically identical.
    2.  Get three male to female wires. Plug them into the D, V, and G of the PCB.
    3.  Connect these to the motor cable of the first (shoulder rotation) Dynamixel with G being connected to Pin 1, V to Pin 2, and D to Pin 3. (Hint: The cable connector has a small 1, 2, and 3 on it so you can identify each pin).
    4.  Plug in the PWR using the 5V power source, and connect the USB-C connector to your computers.

![Leader Electrical Diagram](./pictures/Leader_Arm_Electrical_Diagram.png)

### Follower Arm

| Part | Amount | Unit Cost (US) | Buy US | Unit Cost (EU) | Buy EU | Unit Cost (UK) | Buy UK |
|---|---|---|---|---|---|---|---|
| Dynamixel XL430-W250-T |  2 | $50 | [Robotis](https://www.robotis.us/dynamixel-xl430-w250-t) | 57-61€ | [MyBotShop](https://www.mybotshop.de/DYNAMIXEL-XL430-W250-T)-[GenRobots](https://www.generationrobots.com/en/402823-dynamixel-xl430-w250-t-servomotor.html) | £47 | [RoboSavvy](https://robosavvy.co.uk/dynamixel-xl430-w250-t.html)
| Dynamixel XL330-M288-T |  4 | $24  | [Robotis](https://www.robotis.us/dynamixel-xl330-m288-t) | 40-46€ | [MyBotShop](https://www.mybotshop.de/DYNAMIXEL-XL330-M288-T)-[GenRobots](https://www.generationrobots.com/en/403817-dynamixel-xl330-m288-t-servo-motor.html) | £27 | [RoboSavvy](https://robosavvy.co.uk/robotis-dynamixel-xl330-m288-t.html) |
| XL330 Frame and Idler Wheel 4pcs set |  1 | $10 | [Robotis](https://www.robotis.us/fpx330-h101-4pcs-set) | 12€ | [GenRobots](https://www.generationrobots.com/en/403860-FPX330-H101-hinge-frame-and-idler-set-dynamixel-xl330.html) | £10 |  [RoboSavvy](https://robosavvy.co.uk/fpx330-h101-4pcs-set.html) |
| XL430 Idler Wheel set | 1 | $7 | [Robotis](https://www.robotis.us/hn11-i101-set) | 9€ | [GenRobots](https://www.generationrobots.com/en/403206-hn11-i101-horn-set.html) | £7 | [Robosavvy](https://robosavvy.co.uk/hn11-i101-set.html)|
| Waveshare Serial Bus Servo Driver Board | 1 | $10 | [Amazon](https://a.co/d/7C3RUYU) | 6€ | [Eckstein](https://eckstein-shop.de/WaveShare-Serial-Bus-Servo-Driver-Board-for-ST-SC-Serial-Bus-Servos-EN) | £8 | [Amazon](https://www.amazon.com/Waveshare-Integrates-Control-Circuit-Supports/dp/B0CTMM4LWK/)|
| Voltage Reducer | 1 | $14 | [Amazon](https://www.amazon.com/EPLZON-Converter-5V-5-3V-Transformer-Regulator/dp/B09R4DBZJK) | 7€ | [Amazon](https://www.amazon.fr/ICQUANZX-Converter-Transformer-Voltage-Regulator/dp/B07RGB2HB6) | £11 | [Amazon](https://www.amazon.com/EPLZON-Converter-5V-5-3V-Transformer-Regulator/dp/B09R4DBZJK) |
| 12V Power Supply | 1 | $12 | [Amazon](https://a.co/d/40o8uMN) | 15-36€ | [Amazon](https://www.amazon.fr/LEDMO-Alimentation-Adaptateur-Transformateurs-Chargeur/dp/B07PGLXK4X)-[GenRobots](https://www.generationrobots.com/en/400866-smps-charger-for-bioloid-and-dynamixel-robotis.html) | £9 | [Amazon](https://a.co/d/40o8uMN) |
| Jumper Wires 3*40 pcs set (M-M, M-F, F-F) | 1 | $7 | [Amazon](https://a.co/d/hQfk2cb) | 9€ | [Amazon](https://www.amazon.fr/AZDelivery-Jumper-Cavalier-C%C3%A2ble-Arduino/dp/B074P726ZR) | £5 | [Amazon](https://a.co/d/hQfk2cb) |
| Table Clamp | 1 | $6 | [Amazon](https://a.co/d/4KEiYdV) | n/a | n/a | £5 | [Amazon](https://a.co/d/4KEiYdV) |
| Table Clamp 4pcs set (1 needed)| 1 | n/a | n/a | 14€ | [Amazon](https://www.amazon.fr/CAUTIOUS-Serre-Joint-R%C3%A9glable-Serre-Joints/dp/B0CJMB3SKH) | n/a | n/a |
| 1.5mm Star/Cruciform Screwdriver 2pcs set (1 pc needed) | 1 | n/a | n/a | 7€ | [Amazon](https://www.amazon.fr/sourcing-map-Cruciforme-%C3%89lectroniques-R%C3%A9paration/dp/B0BQ69J2QF) | n/a | n/a |
| 1.5mm Star/Cruciform Screwdriver included in set | 1 | $6 | [Amazon](https://www.amazon.com/Choice-9-Piece-Precision-Screwdriver-Phillips/dp/B0747DYJJR) | n/a | n/a | £5 | [Amazon](https://www.amazon.com/Choice-9-Piece-Precision-Screwdriver-Phillips/dp/B0747DYJJR) |
| USB C-A or C-C 2pcs set (1 pc needed) | 1 | $9 | [Amazon](https://www.amazon.com/Charging-etguuds-Charger-Braided-Compatible/dp/B0B8NWLLW2/) | 7€ | [Amazon](https://www.amazon.fr/-/en/dp/B0CKPDZ3SK/) | £7 | [Amazon](https://www.amazon.com/Charging-etguuds-Charger-Braided-Compatible/dp/B0B8NWLLW2/)|
| Total | | $277 | | 360€ | | £269 | |

Video of the Assembly: [GoogleDrive](https://drive.google.com/file/d/1uk6JFVT2OoHBs3-S-JOH1AkEEqhCJtGh/view?usp=drive_link) #TODO: Update with Youtube Video later.

1. Order all off the shelf parts from the BILL_OF_MATERIALS.md.
2. Print all parts with a 3D printer.
   1. The STL files are in `hardware/follower/STL`
   2. Precision: 0.2mm minimum height layer
   3. Material: PLA, ABS, PETG or other reasonably strong plastics.
   4. Suggested: Prusa Mini+, Bambu P1, Ender3, etc.
3.  Scan each motor.
    1.  Connect the driver board to a computer (should work with Linux and MacOS)
    2.  Figure out the device name (e.g. tty.usbmodem57380045631 for MacOS): ```ls /dev/tty.*```
    3.  Scan each motor individually with [Dynamixel Wizard](https://emanual.robotis.com/docs/en/software/dynamixel/dynamixel_wizard2/)
        1. Set the baudrate to 1M for all motors
        2. Set the servo IDs to 1 for the shoulder to 5 (6 if using the elbow-to-wrist extension) for the gripper servo
4.  Follower the video to in assembling the mechanical structure.
5. Follower the video to in assembling the mechanical structure. #TODO(jess-moss): Should I add more info here? 
6.  Use the electrical diagram to wire the robot
    1.  Use the 6 Dynamixel motor cables to daisy chain the four XL330 motors together and the two XL430 motors together. Do not connect the XL430 motor to the XL 330 motor.
    2.  Get three male to female wires. Plug them into the D, V, and G of the PCB.
    3.  Connect these to the motor cable of the first (shoulder rotation) Dynamixel XL430 with G being connected to Pin 1, V to Pin 2, and D to Pin 3. (Hint: The cable connector has a small 1, 2, and 3 on it so you can identify each pin).
    4.  Get three more male to female wires. Plug them into the second port D, V, and G of the PCB.
    5.  Connect the V to IN+ and G to IN- of the DC Converter.
    6.  Connect the motor cable of the first Dynamixel XL330 (i.e. wrist extention rotation) by connecting Pin 1 to OUT- of the DC converter, Pin 2 connected to OUT+ of the DC converter and Pin 3 connected to D from the second port of the PCB. 
    7.  Plug in the PWR using the 12V power source, and connect the USB-C connector to your computers.

![Follower Diagram](./pictures/Follower_Arm_Electrical_Diagram.png)