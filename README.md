# RoboticsAsCode

**Robotics as Code** (RaC) is using source code to manage and deploy code and configurations to robots.
<br><br>These are the ideals of RaC:

- ROS nodes should be placed in Docker containers.
- Docker containers should be managed by Ansible preferably as Roles.
- Ansible configures settings such as networking

# Links

Examples of RaC implementations

## Docker ROS Links

- [![CI](https://github.com/frankjoshua/docker-ros-master/workflows/CI/badge.svg)](https://github.com/frankjoshua/docker-ros-master/actions) [https://github.com/frankjoshua/docker-ros-master](https://github.com/frankjoshua/docker-ros-master)
- [![CI](https://github.com/frankjoshua/docker-ros-bridge-suite/workflows/CI/badge.svg)](https://github.com/frankjoshua/docker-ros-bridge-suite/actions) [https://github.com/frankjoshua/docker-ros-bridge-suite](https://github.com/frankjoshua/docker-ros-bridge-suite)
- [https://github.com/frankjoshua/docker-ros-turtlesim](https://github.com/frankjoshua/docker-ros-turtlesim)
- [![CI](https://github.com/frankjoshua/docker-ros-desktop/workflows/CI/badge.svg)](https://github.com/frankjoshua/docker-ros-desktop/actions) [https://github.com/frankjoshua/docker-ros-desktop](https://github.com/frankjoshua/docker-ros-desktop)
- [![CI](https://github.com/frankjoshua/docker-ros-jupyter/workflows/CI/badge.svg)](https://github.com/frankjoshua/docker-ros-jupyter/actions) [https://github.com/frankjoshua/docker-ros-jupyter](https://github.com/frankjoshua/docker-ros-jupyter)
- [https://github.com/frankjoshua/docker-ros-tfwebrepublisher](https://github.com/frankjoshua/docker-ros-tfwebrepublisher)
- [https://github.com/frankjoshua/docker-ros-movebase](https://github.com/frankjoshua/docker-ros-movebase)
- [https://github.com/frankjoshua/docker-ros-realsense](https://github.com/frankjoshua/docker-ros-realsense)
- [![Build Status](https://travis-ci.org/frankjoshua/docker-ros-jviz.svg?branch=master)](https://travis-ci.org/frankjoshua/docker-ros-jviz) [https://github.com/frankjoshua/docker-ros-jviz](https://github.com/frankjoshua/docker-ros-jviz)
- [![Build Status](https://travis-ci.org/frankjoshua/docker-ros-webviz.svg?branch=master)](https://travis-ci.org/frankjoshua/docker-ros-webviz) [https://github.com/frankjoshua/docker-ros-webviz](https://github.com/frankjoshua/docker-ros-webviz)
- [![CI](https://github.com/frankjoshua/docker-ros-m1m1/workflows/CI/badge.svg)](https://github.com/frankjoshua/docker-ros-m1m1/actions) [https://github.com/frankjoshua/docker-ros-m1m1](https://github.com/frankjoshua/docker-ros-m1m1) (x86 only)

## Ansible Role Links

- [![Build Status](https://travis-ci.org/frankjoshua/ansible-role-ros-master.svg?branch=master)](https://travis-ci.org/frankjoshua/ansible-role-ros-master) [https://github.com/frankjoshua/ansible-role-ros-master](https://github.com/frankjoshua/ansible-role-ros-master)
- [https://github.com/frankjoshua/ansible-role-ros-adafruitmotorhat](https://github.com/frankjoshua/ansible-role-ros-adafruitmotorhat)
- [https://github.com/frankjoshua/ansible-role-ros-velocity-muxer](https://github.com/frankjoshua/ansible-role-ros-velocity-muxer)
- [https://github.com/frankjoshua/ansible-role-ros-bridge-suite](https://github.com/frankjoshua/ansible-role-ros-bridge-suite)
- [https://github.com/frankjoshua/ansible-role-ros-slamtec-m1m1](https://github.com/frankjoshua/ansible-role-ros-slamtec-m1m1)

## Raspberry Pi Links

- [https://github.com/frankjoshua/docker-uv4l](https://github.com/frankjoshua/docker-uv4l)
- [https://github.com/frankjoshua/ansible-role-rpi-uv4l](https://github.com/frankjoshua/ansible-role-rpi-uv4l)

# Notes

## Example of a catkin workspace in docker

[https://github.com/frankjoshua/docker-ros-bridge-suite](https://github.com/frankjoshua/docker-ros-bridge-suite)

## Demo of ROS in Jupyter Notebook

[https://github.com/frankjoshua/demo-ros-cmdvel-jupyter](https://github.com/frankjoshua/demo-ros-cmdvel-jupyter)

[![](https://img.youtube.com/vi/cztepMA39Ik/0.jpg)](https://www.youtube.com/watch?v=cztepMA39Ik)

## Example:

Add roles to requirements.yml

```
- src: https://github.com/frankjoshua/ansible-role-ros-master.git
- src: https://github.com/frankjoshua/ansible-role-ros-adafruitmotorhat.git
```

Install with ansible galaxy

```
ansible-galaxy install -r ./ansible/requirements.yml
```

Then you can use as normal ansible roles

```
  roles:
    - role: ansible-role-ros-master
    - role: ansible-role-ros-adafruitmotorhat
```

#

###

## Follow me [@frankjoshua77](https://twitter.com/frankjoshua77)
