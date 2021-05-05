
# Dagu Thumper Tour Guide
The main idea of this project is to design a conceptual robot tour guide for an art gallery using Dagu Thumper. The kit's task is to scan the art space, detect the exibits by detecting their color, recall background information and give the visitors a brief description about the history of the art piece, e.x. artist, period, location ..etc.

## Motivation 
Social robots has been recently used to serve multiple purposes, like personal assistance and performing tasks within the domain of domestic services and healthcare. Currently, there is a growing interest in the use of tour guide mobile robots in various environments such as museums, exhibitions and fairs, to provide help for the visitors by offering them a set of services, such as giving them general tours, helping them find points of interest, and providing information about different exhibits.

## Initial Design 
### Features
* Text-to-Speech: By Giving a Brief Description about an Art Piece.
* Color detection: To recognize the art piece through dtecting different colors.
* Obstacle Detection: To Avoid Collision.

### Logic Design
![Logic Design](https://i.imgur.com/Y2jsA25.png)

### System Design
![System Design](https://i.imgur.com/HXbgxBY.png)

## Hardware Platform   
In this project, we are planning to use Segway Loomo primarily making use of the following sensors and actuators, as shown in the figure:
### Sensors
* The microphone array: which is composed of 5 mics is used to localize voice source and reduce background noises during voice recognition.
* The Ultrasonic sensor: in the front to detect obstacles in real time to prevent collisions.
* Intel's RealSense module: to provide aligned RGB-Depth images at 30fps, for visual Simultaneous Localization and Mapping (SLAM).
* The main HD camera: which is mounted next to the robot face, with a wide-angle of 104 degrees FOV.
### Actuators
* Speakers
* Wheel Motors  
* LCD Screen: for output displaying and debugging purposes.   
![Hardware Platform](https://i.imgur.com/Ue1aABD.png) 


## Software Platform 
Since Loomo runs on the Android version 5.1 operating system, we will need to use Android Studio as a development tool.
we'll use the Loomo SDK mainly focusing on the:
* Speech SDK
* Vision SDK
* Locomotion (Base) SDK 

## Initial Assumptions
* The map of the gallery is predefined and positions of exhibits .
* The human interaction partners follow the robot’s suggestions without the need for the robot to check for their compliance.

## Challenges and Modifications 
1. We decided not to proceed working with Loomo Segway for number of reasons. These includes the inability to deploy native C++ robotics applications on Loomo robot. The only Repository found hat works as a bridge between JAVA SDK and C++ interfaces was in alpha phase with no sufficient documentation and number of deprecated modules/libraries. 
2. The is no resources found that explain interfacing between our color sensor(TCS230) and our microcontroller (stm32l432kc). However, There are alot of support when using Arduino. So we were able to operate on Arduino to test our hypothesis . We used the sensor with stm32l432kc board, but the results are not very accurate. 

## Milestones
1. First Milestone (A Predefined Path Following & Speaking Features & obstacles detection): Using a previously known localization map, the Dugo Thumper can guide the users and give them information about different exhibits, following a predefined path from start to end along with avoiding any obstacle in its way. 
2. Second Milestone (Art pieces detection & Information Retrieval Feature): We will utilize the color sensor to detect the exhibits and then retrieve the related information. 
3. Third Milestone (Point-to-Point Mapping Feature): In this milestone, we shall add the feature of the robot being able to direct the users to their desired art piece from a any point in the exhibition. The User shall send the name of the art piece tp the kit trough Bluetooth Module. 


## References
*


## Proposal Video
Kindly, find the proposal video at [this link](https://drive.google.com/file/d/1foOe66EDGX7r4gehLcNGmYwh58q4fUl_/view?usp=sharing).  
For the slides, check [this link](https://drive.google.com/file/d/1M-g5JhZSnqB3LKiKBddfGtiu3rjULKN2/view?usp=sharing).

## Team Members
* Hadeel Mabrouk - 900163213
* Israa Fahmy - 900171831
* Samah Ayman - 900171848
