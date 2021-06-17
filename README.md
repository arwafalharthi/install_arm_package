# install_arm_package
To install the arm package,we need to go to src ,install git and then install the package :
```
$ cd catkin_ws/src
$ sudo apt install git
$ git clone https://github.com/smart-methods/arduino_robot_arm
```
Now install the dependencies 
```
$ cd catkin_ws
```
```
rosdep install --from-paths src --ignore-src -r -y
```
```
$ sudo apt-get install ros-melodic-moveit
$ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
$ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
$ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
```
To compile the packege
```
$catkin_make
```
after finshing the installing we open it by type :
```
roslaunch robot_arm_pkg_motors.launch
```
## after run
![ArmPkgRViz](https://user-images.githubusercontent.com/85634104/122269436-e03f2780-cee5-11eb-9ad0-939f7e628bbb.png)
