# Unodopo

## Description
This repository contains the packages that are required to run our modified version of the Unodopo robot. Our modified version of the robot runs using the [roboteq motor controller](https://www.roboteq.com/index.php) and the [sick lidar](https://www.sick.com/za/en/detection-and-ranging-solutions/2d-lidar-sensors/tim5xx/c/g292754)

## Teleoperations
To run teloperations on the robot run:
```
roslaunch unodopo_bringup unodopo_core_hardware.launch 
```
followed by your teleoperation controller of choice.

## Lidar
```
roslaunch unodopo_bringup unodopo_lidar.launch hostname:=192.168.0.123 frame_id:=laser_scan_link

```

## Navigation
```
roslaunch unodopo_bringup unodopo_core_hardware.launch
roslaunch unodopo_bringup unodopo_lidar.launch hostname:=192.168.0.123 frame_id:=laser_scan_link
roslaunch unodopo_navigation unodopo_navigation.launch
```

## RVIZ
To vew your robot's URDF in Rviz
```
roslaunch unodopo_description display.launch
```