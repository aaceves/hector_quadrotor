# hector_quadrotor

Hector-Quadrotor is a series of packages developed by the Institute for Flight Systems and Automatic Control at the Technical University of Darmstadt in Germany for ROS and GAZEBO. The most recent version of Hector-Quadrotor was released in 2018 for ROS Kinetic [1], but thanks to various contributors, it can also be installed for ROS Melodic [2] and ROS Neotic [3].


## Requirments

Run these commands in a Terminal, one by one:
```
sudo apt-get install ros-melodic-geographic-info
sudo apt-get install ros-melodic-ros-control
sudo apt-get install ros-melodic-gazebo-ros-control
sudo apt-get install ros-melodic-joy
sudo apt-get install ros-melodic-teleop-twist-keyboard
```

## Instalation

The process to install Hector-quadrotor is the following;
```
mkdir ~/hector_ws
cd ~/hector_ws
git clone https://github.com/aaceves/hector_quadrotor.git
mv hector_quadrotor src
```
You will need to install some missing dependencies:
```
sudo apt update
rosdep install --from-paths src --ignore-src –r 
```
Finally, compile and declare the new packages:
```
cd ~/hector_ws
catkin_make
source devel/setup.bash
```

## Run a first demo

You can run some demos by executing the launch files in hector_quadrotor_gazego and hector_quadrotor_demo packages.
In one terminal, try:
```
roslaunch hector_quadrotor_gazebo quadrotor_empty_world.launch
```

## References

1. Technische Universität Darmstadt, "hector_quadrotor", Germnay, Jun 2018, Kinetic: https://github.com/tu-darmstadt-ros-pkg/hector_quadrotor 
2. Basavaraj Navalgund, "Hector-quadrot for ROS Melodic", India, Sep 2002, https://github.com/basavarajnavalgund/hector-quadrotor 
3. RAFALAMAO, "hector_quadrotor ported to ROS Noetic & Gazebo 11", Mexico Feb 2022, Neotic: https://github.com/RAFALAMAO/hector_quadrotor_noetic 
