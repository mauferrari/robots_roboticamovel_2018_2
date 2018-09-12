# robots_roboticamovel_2018_2
Repo with the robots used at the Mobile Robotic Class 2018-2

Stage sim             |  Rviz visualization
:-------------------------:|:-------------------------:
![system](img/pioneer_stage_v1.png) <!-- .element width="200" -->  |  ![system](img/pioneer_v1.png) <!-- .element width="200" -->

### Installation

This setup was tested in ROS Kinetic, running on Ubuntu 16.04 LTS.

Install the dependencies and devDependencies and start the server.

```sh
$ cd ~/catkin_ws/src/
$ git clone https://github.com/h3ct0r/robots_roboticamovel_2018_2
$ cd ~/catkin_ws/
$ rosdep install --from-paths src/robots_roboticamovel_2018_2 --ignore-src -r -y
$ catkin_make
$ source devel/setup.bash
```

### Running the nodes

There are several options to running the simulations:

- Using a simple differencial robot (Pioneer DX)

    ```sh
    roslaunch robots_roboticamovel_2018_2 simple_differential.launch
    ```

- Using a simple holonomic robot (Turtlebot)

    ```sh
    roslaunch robots_roboticamovel_2018_2 simple_holonomic.launch
    ```
    
Running the teleop node to control the robot with the keyboard:
```sh
rosrun teleop_twist_keyboard teleop_twist_keyboard.py cmd_vel:=/cmd_vel
```

### Todos

 - Write MORE Tests

License
----

MIT


**Free Software, Hell Yeah!**
