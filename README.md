# ros2-dev-container

Adapted shamelessly from [this ROS2 community guide](https://docs.ros.org/en/jazzy/How-To-Guides/Setup-ROS-2-with-VSCode-and-Docker-Container.html).

## Open / Build Dev Container in VSCode
1. Open directory in VSCode
2. `Ctrl+Shift+P` > `Dev Containers: Reopen in Container`

## Verify GUI Bridge

### On Host
```
# Less Safe
xhost +local:
xhost -local:

# More Safe
xhost +SI:localuser:$USER
xhost -SI:localuser:$USER
```

### In Docker
```
sudo apt install ros-$ROS_DISTRO-rviz2 -y
source /opt/ros/$ROS_DISTRO/setup.bash
rviz2
```
