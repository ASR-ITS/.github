# ASR - ITS MANUAL GUIDE

## HOW-TO ASR-ITS Start-Up
Main Control Layout for Service Robot ASR-ITS
```bash
# Launch Main File
cd slam_ws
roslaunch main_controller asr_its.launch

# Use Waypoint Generator if Needed
rosrun path_planning waypoint.py
```


## HOW-TO Connect Sensor and Peripheral
### DualShock 4 Controller
```bash
# Push PS Button on Controller for Bluetooth Auto Connect
# Use this command if Controller not connected, make sure PS Button is pressed
cd
./ds4_autoconnect.sh
```

### STM32 UART and RPLidar
```bash
# Connect STM32 Cable to USB 3.0 Port (make sure it on /dev/ttyUSB0)
# Connect RPLidar Data Cable to Thunderbolt Port
cd 
./chmodbus01.sh
```

### ZED 2i Stereo Camera (Optional)
```bash
# Connect ZED 2i Camera Cable to USB 3.0 Port
# Run ZED 2i Wrapper
roslaunch zed_wrapper zed2i.launch
```


## Dependencies
- ds4_driver https://github.com/naoki-mizuno/ds4_driver
- zed_wrapper https://github.com/stereolabs/zed-ros-wrapper
- rplidar_ros https://github.com/Slamtec/rplidar_ros
