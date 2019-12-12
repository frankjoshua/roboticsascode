# RAC
ROS nodes are placed in Docker containers.<br>
Docker containers are managed as Ansible Roles.

## Docker ROS Links
- [https://github.com/frankjoshua/docker-ros-bridge-suite](https://github.com/frankjoshua/docker-ros-bridge-suite)
- [https://github.com/frankjoshua/docker-uv4l](https://github.com/frankjoshua/docker-uv4l)
- [https://github.com/frankjoshua/docker-ros-turtlesim](https://github.com/frankjoshua/docker-ros-turtlesim)
- [https://github.com/frankjoshua/docker-ros-desktop](https://github.com/frankjoshua/docker-ros-desktop)

## Anisible Role Links
- [https://github.com/frankjoshua/ansible-role-ros-master](https://github.com/frankjoshua/ansible-role-ros-master)
- [https://github.com/frankjoshua/ansible-role-ros-adafruitmotorhat](https://github.com/frankjoshua/ansible-role-ros-adafruitmotorhat)
- [https://github.com/frankjoshua/ansible-role-ros-velocity-muxer](https://github.com/frankjoshua/ansible-role-ros-velocity-muxer)

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