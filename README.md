# raspimouse_virtualjoystick_webcontroller
Remotely control Raspberry Pi Mouse using web browser application

## movie 
https://www.youtube.com/watch?v=Mg4MFJgvnHc

## Requirement
This package requires the following to run:  
* Camera LOGICOOL C270  
* Ubuntu  
    Ubuntu 16.04 (Ubuntu 16.04 Server recomended)  
* ROS  
    Kinetic Kame  
* ROS package
  * ros-kinetic-cv-bridge
  * ros-kinetic-cv-camera
  * ros-kinetic-image-transport-plugins
  * rosbridge_suite

## Installation

First of all, install the latest stable version of ROS.  
Please refer to ROS WiKi for installation.  
Next, download the dependent ROS package into ~/catkin_ws/src and build it  

    cd ~/catkin_ws/src
    git clone https://github.com/ryuichiueda/raspimouse_ros_2.git
    cd ~/catkin_ws && catkin_make && source ~/catkin_ws/devel/setup.bash

Next, USB connection between webcam and robot and download this repository and build it.

    sudo apt install ros-kinetic-cv-bridge
    sudo apt install ros-kinetic-cv-camera
    sudo apt install ros-kinetic-image-transport-plugins
    cd ~/catkin_ws/src
    git clone https://github.com/RobotWebTools/mjpeg_server.git
    cd ~/catkin_ws && catkin_make && source ~/catkin_ws/devel/setup.bash
    
Finaly, download this repository and build it and install this package.

    cd ~/catkin_ws/src
    git clone https://github.com/iidayuki/raspimouse_virtualjoystick_webcontroller.git
    sudo apt install ros-kinetic-rosbridge-suite
    cd ~/catkin_ws && catkin_make && source ~/catkin_ws/devel/setup.bash 
    
## Usage
To use this script with raspimouse_ros_2, input the following commands.

    $ roscore
    
In another terminal

    $ roslaunch raspimouse_controller raspimouse_controller.launch 

Open the browser: 
    http:// localhost :8000
    


## License
MIT License
### Includings & References
* [RobotWebTools/mjpeg_server]( https://github.com/RobotWebTools/mjpeg_server ) - BSD 3-clause
  * launch/*
  
* [jeromeetienne/virtualjoystick.js]( https://github.com/jeromeetienne/virtualjoystick.js ) - MIT
  * contents/virtualjoystick.js

* https://github.com/twbs/bootstrap - MIT
  * contents/css/*
  * contents/fonts/*
  * contents/js/*

* [ryuichiueda/pimouse_monitor]( https://github.com/ryuichiueda/pimouse_monitor ) - MIT 
  * contents/index.html
  * contents/main.js
  * launch/*
  * scripts/*
  
* [RobotWebTools/roslibjs]( https://github.com/RobotWebTools/roslibjs ) - BSD 3-clause
  * contents/index.html

* [jquery/jquery]( https://github.com/jquery/jquery ) - MIT 
  * contents/index.html
  * contents/main.js
