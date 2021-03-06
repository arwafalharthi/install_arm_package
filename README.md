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
after install, open it by :
```
roslaunch robot_arm_pkg_motors.launch
```
![ArmPkgRViz](https://user-images.githubusercontent.com/85634104/122269436-e03f2780-cee5-11eb-9ad0-939f7e628bbb.png)


after install arduino

## Install rosserial
```
$ sudo apt-get install ros-indigo-rosserial-arduino
$ sudo apt-get install ros-indigo-rosseria
```
## Install ros_lib into the Arduino Environment
```
$ cd Arduino/libraries
$ rm -rf ros_lib
$ rosrun rosserial_arduino make_libraries.py
```
### instructions to use gazebo
in terminal
```
$ cd catkin_ws
$ source devel/setup.bash
$ roslaunch robot_arm_pkg check_motors.launch
```
in other terminal 
```
$ cd catkin_ws
$ source devel/setup.bash
$ roslaunch robot_arm_pkg check_motors_gazebo.launch
```
in other terminal,change the premission
```
$ cd catkin_ws/src/arduino_robot_arm/robot_arm_pkg/scripts
$ sudo chmod +x joint_states_to_gazebo_py
```
then 
```
$ cd catkin_ws
$ source devel/setup.bash
$ rosrun robot_arm_pkg joint_states_to_gazebo.py
```
![joinrvisgazebo](https://user-images.githubusercontent.com/85634104/122645046-df460a00-d120-11eb-94d7-2c6c6837da52.png)

This will run gazebo and RViz in moveit
```
roslaunch moveit_pkg demo_gazebo.launch
```

Result

![gazeporvizMovitB](https://user-images.githubusercontent.com/85634104/122688187-7d21fd80-d223-11eb-82db-2e7ac440f7e6.png)
![gazeporvisMoveitA](https://user-images.githubusercontent.com/85634104/122688255-e86bcf80-d223-11eb-9ee4-9a1ff9bc7edb.png)


