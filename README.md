# RoboticsAsCode
**Robotics as Code** (RaC) is using source code to manage and deploy code and configurations to robots.
<br><br>These are the ideals of RaC: 
- ROS nodes should be placed in Docker containers.
- Docker containers should be managed by Ansible preferably as Roles.
- Ansible configures settings such as networking

# Links
Examples of RaC implementations
## Docker ROS Links
- [https://github.com/frankjoshua/docker-ros-bridge-suite](https://github.com/frankjoshua/docker-ros-bridge-suite)
- [https://github.com/frankjoshua/docker-ros-turtlesim](https://github.com/frankjoshua/docker-ros-turtlesim)
- [https://github.com/frankjoshua/docker-ros-desktop](https://github.com/frankjoshua/docker-ros-desktop)
- [https://github.com/frankjoshua/docker-ros-jupyter](https://github.com/frankjoshua/docker-ros-jupyter)

## Ansible Role Links
- [https://github.com/frankjoshua/ansible-role-ros-master](https://github.com/frankjoshua/ansible-role-ros-master)
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