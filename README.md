# RoboticsND_Map_My_World
Implement the RTAB-Map algorithm on a robot and create a 3-D map of my world (based on RoboticsND_Build_My_World)

![rtab](RTAB-Map_Database_Viewer.png)

## Instructions

1. Create and initialize a catkin workspace `catkin_ws`
```
mkdir -p /***preferred directory***/catkin_ws/src  
cd /***preferred directory***/catkin_ws/src  
catkin_init_workspace  
```

2. Clone this repo in a different directory and move all files/folders to `catkin_ws/src`
```
cd /***preferred directory***  
git clone https://github.com/azzamshaikh/RoboticsND_Map_My_World  
```

3. Due to the large size of the map.pgm file, they were zipped and will need to be unzipped
```
cd /***preferred directory***/catkin_ws/src/my_robot/maps  
unzip map.zip && rm map.zip  
```

4. Add teleop package to the `src` directory
```
cd /***preferred directory***/catkin_ws/src  
git clone https://github.com/ros-teleop/teleop_twist_keyboard
````

3. Go back to the `catkin_ws` directory and and launch the world/teleop packages and mapping algorithm. You will need two terminals.
```
cd /catkin_ws  
catkin_make  
source devel/setup.bash  
roslaunch main main.launch
```
```
cd /catkin_ws  
source devel/setup.bash  
roslaunch my_robot mapping.launch
```
4. To open the RTAB-MAP database, the file can be found here: (https://drive.google.com/file/d/1iOatuBzopqTjq7I3WaE0TP4tGlxg-5Qk/view?usp=sharing). Please copy the file into the src file and open. 
```
rtabmap-databaseViewer /***preferred directory***/catkin_ws/src/rtabmap.db
```
5. The mesh generated from the database viewer is also available here: (https://drive.google.com/file/d/1PyacnGWZnS114Pl63yGpIUMCphqGjChL/view?usp=sharing)
