# hector_quadrotor

It is a set of packages for modeling, control and simulation of quadrotor UAV systems.

## Description

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

1. Kinetic: https://github.com/tu-darmstadt-ros-pkg/hector_quadrotor 
2. Melodic: https://github.com/basavarajnavalgund/hector-quadrotor 
3. Neotic: https://github.com/RAFALAMAO/hector_quadrotor_noetic 
