# ICCPS25: Enabling Close-to-Minimum Separation Distances between Small Autonomous Rotor-craft using Ubiquitous Built-in Sensor

## Abstract
The increasingly widespread deployment of autonomous small uncrewed aerial systems (sUAS), particularly rotor-craft, in close proximity to one another, introduces the real danger of mid-air collisions. In practice, many sUAS `fly blind' with minimal capabilities for detecting and avoiding fast-moving aerial objects. While LIDAR or multi-direction cameras can provide accurate, real-time distance measurements of ground-based obstacles and other airborne vehicles, their weight and power consumption can limit the flight-time of small drones, and place demands upon limited processing resources. We propose an alternative approach that leverages existing sensor data and inter-drone communication to reliably provide awareness of close neighbors and to dynamically compute safe minimum separation distance between sUAS. This allows sUAS, even without high-performing LIDAR to coordinate their movements in relatively close quarters to one another.  Our method uses a vectorized representation of safety margins through Oriented Bounding Boxes (OBBs) computed based on geolocation uncertainty, wind-conditions, physical capabilities of each sUAS, and other factors to dynamically determine and adapt minimum separation distances using ubiquitous sensor data provided by PX4 and/or Ardupilot flight controllers. Through high-fidelity Monte Carlo simulations, we demonstrated that our approach effectively prevents collisions, with drones maintaining safe separation based solely on flight controller data and inter-drone communication. Variable-rate status messages reduced CPU load and bandwidth consumption by up to 74\% and 67\%, respectively. In addition, our method remained robust even under severe network conditions with high message drop rates. These findings suggest that our approach provides a scalable and viable solution for mid-air collision avoidance in sUAS that offers a lightweight alternative to sensor-heavy systems.

## Animation Sample
For all video samples below, we utilized the High Fideloty Gazebo simulation environment in conjunction with PX4 to collect telemetry data and analyze OBB's dynamic size as drones performed numerous maneuvers and tasks. Using the collected and processed telemetry data, we reconstructed a playback animation in Matplotlib. For each sample, we provide its corresponding Ulog. 


### 1
Description: Drone performing a variety of maneuvers, including takeoff, flywaypoints, circle and land. 

https://github.com/user-attachments/assets/bd12ccb5-8246-4e74-97d2-8e843a4f2d16

| ID      | Ulog File Link | 
|---------|----------------|
| Red     | [Link to ulog](https://review.px4.io/plot_app?log=3196ae1e-1583-4948-91a8-83ef265f329f) | 



### 2
Description: Two drones approaching at high speed towards the same converging point. 

https://github.com/user-attachments/assets/2c2c3b64-60f1-462b-826d-d00fad838357

Associated PX4 Ulog

| ID      | Ulog File Link | 
|---------|----------------|
| Red     | [Link to ulog](https://review.px4.io/plot_app?log=f77f8f2a-dc55-4925-a73f-a9eb008a5414) | 
| Lime    | [Link to ulog](https://review.px4.io/plot_app?log=59a67df6-4e09-4278-9c4b-985c04533c3d) | 
