# UVDAR drivers and processing [![Build Status](https://travis-ci.com/ctu-mrs/uvdar.svg?branch=master)](https://travis-ci.com/ctu-mrs/uvdar)

![](.fig/thumbnail.jpg)

## Description

* the UVDAR system is a visual mutual relative localization system for cooperating micro-scale UAVs
* based on ultraviolet-sensitive cameras and blinking ultraviolet markers
* can be used both indoors and outdoors without infrastructure
* robust to a variety of lighting conditions

## System requirements

#### Hardware:
* One or more calibrated (Using the OCamCalib model) grayscale camera sensors with ultraviolet bandpass filters. In our setup these are:
  * mvBlueFOX MLC200wG cameras
  * Sunnex DSL215 lenses with ~180 degrees of horizontal FOV 
  * Midopt BP365-R6 filters with our custom holder between the sensor and the lens

* Blinking ultraviolet LEDs (395nm) attached to extreme points of the target UAVs. In our setup, these are:
  * ProLight Opto PM2B-1LLE
  * Attached to the ends of the arms of the UAVs, respectively on the top of the UAVs for "beacons"
  * For quadrotors, the markers comprise two LEDs each, rotated 90&deg; from each other in the "yaw" axis of the UAV

#### Software
  * [ROS (Robot Operating System)](https://www.ros.org/) Melodic Morenia
  * [mrs_lib](https://github.com/ctu-mrs/mrs_lib) - ROS package with utility libraries used by the MRS group
  * [mrs_msgs](https://github.com/ctu-mrs/mrs_msgs) - ROS package with message types used by the MRS group
  * [bluefox2](https://github.com/ctu-mrs/bluefox2) - ROS package providing interface with mvBlueFOX cameras

#### Included third party libraries
  * [OCamCalib](https://sites.google.com/site/scarabotix/ocamcalib-toolbox) calibration system by Davide Scaramuzza - only the C++ sources
  * [P3P](https://www.laurentkneip.com/software) library by Laurent Kneip

#### For testing in simulation
  * [mrs_uav_system](https://github.com/ctu-mrs/mrs_uav_system) Our ROS-based ecosystem for flying and testing multi-UAV systems

