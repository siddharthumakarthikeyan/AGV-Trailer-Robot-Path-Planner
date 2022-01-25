# AGV-Trailer-Robot-Path-Planner
Autonomous Path Planning of Trailer based AGV with obstacle avoidance

### System Dependencies
- Ubuntu : 20.04+
- ROS : Noetic+
- CPU : ARM7+ or Intel i3+ or AMD R4+
- RAM : 4GB+
- Memory : 10GB+

### Dependencies

- ```sudo apt-get install ros-noetic-gmapping```
- ```sudo apt-get install ros-noetic-teleop-twist-keyboard```
- ```sudo apt-get install ros-noetic-sbpl```
- ```sudo apt-get install ros-noetic-teb-local-planner```
- ```sudo apt-get install ros-noetic-global-planner```
- ```sudo apt-get install ros-noetic-map-server```
- ```sudo apt-get install ros-noetic-move-base```

### steps to runs 
*note* Run the scripts in the following sequence

- Terminal 1 -
    - mkdir AGV_Trailer
    - cd AGV_Trailer
    - git clone https://github.com/siddharthumakarthikeyan/AGV-Trailer-Robot-Path-Planner.git
    - catkin_make
- Terminal 2 -
    - source ~/AGV_Trailer/devel/setup.bash
    - roscore
- Terminal 3 -
    - source ~/AGV_Trailer/devel/setup.bash
    - cd Coppeliasim/
    - ./coppeliasim.sh (launches coppelia sim)
    - load the scene from `~/AGV_Trailer/src/coppeliasim_ws/vrep_scenes/`
- Terminal 4 -
    - source ~/AGV_Trailer/devel/setup.bash
    - roslaunch coppeliasim_ws teleop.launch
- Terminal 5 -
    - source ~/AGV_Trailer/devel/setup.bash
    - roslaunch coppeliasim_ws mapping.launch
- Terminal 6 -
    - source ~/AGV_Trailer/devel/setup.bash
    - roslaunch coppeliasim_ws nav.launch
    - send goals via rviz


