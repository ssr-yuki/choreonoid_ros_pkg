About
-----

This repository provides ROS support for Choreonoid

choreonoid\_ros\_pkg: Chorenoid catkin package

choreonoid\_plugin: Choreonoid plugins to publish ROS topic


Usage
-----

Make sure you have installed wstool and catkin

```
$ sudo apt-get install python-wstool python-catkin-tools
```

Create catkin workspace

```
$ mkdir -p catkin_ws/src
$ cd catkin_ws/src
$ wstool init
```

Checkout choreonoid\_ros\_pkg

```
$ wstool set choreonoid_ros_pkg https://github.com/fkanehiro/choreonoid_ros_pkg.git --git
$ wstool update choreonoid_ros_pkg
```

Build

```
$ cd ~/catkin_ws
$ catkin build choreonoid_ros
$ catkin build choreonoid_plugins
```

Run

```
$ roscore (on the different terminal)
$ ./devel/bin/choreonoid
```

Configure AISTSimulator item to use High-gain dynamics mode.
Create and place BodyRos item under the robot you want to control.

Each joint states are published to /[robotname]/joint\_states topic.
Your control signal can be sent using /[robotname]/set\_joint\_trajectory topic.


Note
-----

Launchscript and other useful tools will be provided soon.
