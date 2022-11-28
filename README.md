


```
mkdir -p ~/ros/arg_ws/src
git clone https://github.com/autonomousracing-ai/arg_demos ~/ros/arg_ws/src/arg_demos
git clone https://github.com/autonomousracing-ai/arg_devbot_description ~/ros/arg_ws/src/arg_devbot_description
git clone https://github.com/autonomousracing-ai/arg_lidar_distortion_correction ~/ros/arg_ws/src/arg_lidar_distortion_correction
git clone https://github.com/autonomousracing-ai/arg_data_croix_en_ternois ~/ros/arg_ws/src/arg_data_croix_en_ternois
git clone https://github.com/autonomousracing-ai/arg_localization ~/ros/arg_ws/src/arg_localization 

cd ~/ros/arg_ws/src/arg_data_croix_en_ternois/bagfile
tar -xvf devbot_lap0.tar.xz

source /opt/$ROS_DISTRO/setup.bash
cd ~/ros/arg_ws
catkin_make
```



Terminal 1
```
source ~/ros/arg_ws/devel/setup.bash
roscore
```

Terminal 2
```
source ~/ros/arg_ws/devel/setup.bash
roslaunch arg_data_croix_en_ternois play_rosbag.launch 
```

Terminal 3
```
source ~/ros/arg_ws/devel/setup.bash
roslaunch arg_demos arg_demo_lidar_distortion.launch
```

start with space the rosbag in Terminal 2
