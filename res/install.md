## Install
```
mkdir -p stage_ws/src
cd stage_ws/src
git clone https://github.com/CRTA-Lab/Stage.git
git clone https://github.com/CRTA-Lab/stage_ros2.git
rosdep update
rosdep install --from-paths ./Stage --ignore-src -r -y  # install dependencies for Stage
rosdep install --from-paths ./stage_ros2 --ignore-src -r -y  # install dependencies for stage_ros2
cd ~/stage_ws
colcon build --symlink-install 
```

> **Note:** If you see the following warning during the build, you can safely ignore it:
> ```
> CMake Warning:
>   Manually-specified variables were not used by the project:
>
>     CATKIN_INSTALL_INTO_PREFIX_ROOT
>     CATKIN_SYMLINK_INSTALL
> ```
