# xiaomi_lds_myhome





## Cartographer

See: https://google-cartographer-ros.readthedocs.io/en/latest/compilation.html

```bash
$ sudo apt-get install -y python3-wstool python3-rosdep ninja-build stow

$ mkdir catkin_ws
$ cd catkin_ws
$ wstool init src
$ wstool merge -t src https://raw.githubusercontent.com/cartographer-project/cartographer_ros/master/cartographer_ros.rosinstall
$ wstool update -t src
$ sudo rosdep init
$ rosdep update
$ rosdep install --from-paths src --ignore-src --rosdistro=${ROS_DISTRO} -y
$ src/cartographer/scripts/install_abseil.sh

$ catkin build -DCMAKE_BUILD_TYPE=RelWithDebInfo
$ source devel/setup.bash

$ rosrun cartographer_ros cartographer_rosbag_validate -bag_filename $(rospack find xiaomi_lds_myhome)/demo/my_home.bag
```

