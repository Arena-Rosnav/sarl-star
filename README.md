# sarl_star
ROS implementation of the paper [SARL*: Deep Reinforcement Learning based Human-Aware Navigation for Mobile Robot in Indoor Environments](https://ieeexplore.ieee.org/abstract/document/8961764) presented in ROBIO 2019. This mobile robot navigation framework is implemented on a Turtlebot2 robot platform with lidar sensors (Hokuyo or RPlidar), integrating SLAM, path planning, pedestrian detection and deep reinforcement learning algorithms.

**Video demonstration can be found on**   [Youtube](https://youtu.be/izrrctuUd-g) or [bilibili](https://www.bilibili.com/video/av74520445).

## Build & Install
1. Activate poetry shell
```
cd arena-rosnav # navigate to the arena-rosnav directory
poetry shell
```
2. Make sure to source the workspace environment
```bash
cd ../.. # navigate to the catkin_ws directory
source devel/setup.zsh # if you use bash: source devel/setup.bash 
```
3. Install Python-RVO2
```bash
roscd sarl_star_ros
cd ../Python-RVO2
pip install Cython
python setup.py build
python setup.py install
```

4. Install Python dependencies

```
roscd sarl_star_ros
cd CrowdNav/
pip install -e .
```

## Introduction
We present an advanced version of the Socially Attentive Reinforcement Learning (SARL) algorithm, namely SARL*, to achieve human-aware navigation in indoor environments. Recently, deep RL has achieved great success in generating human-aware navigation policies. However, there exist some limitations in the real-world implementations: the learned navigation policies are limited to certain distances associated with the training process, and the simplification of the environment neglects obstacles other than humans. In this work, we improve the SARL algorithm by introducing a dynamic local goal setting mechanism and a map-based safe action space to tackle the above problems. 

## Method Overview
![For more details, please refer to the paper.](https://github.com/LeeKeyu/sarl_star/blob/master/imgs/overview.png)


## System Setup

We use the laser scanner **Hokuyo UTM-30LX** or **RPLIDAR-A2** as the sensor and [**TurtleBot 2**](http://wiki.ros.org/turtlebot/Tutorials/indigo)  as the robot platform.

![](https://github.com/LeeKeyu/sarl_star/blob/master/imgs/system.png)


## Some Experiments
![For more details, please refer to the paper.](https://github.com/LeeKeyu/sarl_star/blob/master/imgs/experiments.png)



## Citation
If you find our work useful in your research, please consider citing our paper:
```
@INPROCEEDINGS{8961764,  
author={K. {Li} and Y. {Xu} and J. {Wang} and M. Q. -. {Meng}},  
booktitle={2019 IEEE International Conference on Robotics and Biomimetics (ROBIO)},   
title={SARL∗: Deep Reinforcement Learning based Human-Aware Navigation for Mobile Robot in Indoor Environments},   
year={2019},  
volume={},  
number={},  
pages={688-694},}
```
## Questions

If you have any questions, please contact "kyli@link.cuhk.edu.hk".


