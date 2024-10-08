# UAV-Visual-Mapping

### Project Description

This project explore the process of 3D slightly hilly terrain reconstruction using UAVs with down-pointing stereo-camera. A mesh reconstruction of area is generated from raw images after UAVs scans this area. The core modules are trajectory planning, feature matching, point cloud generation and merging, colored mesh generation.

<img src="image/enviroment.png" alt="environment" width="400" height="300">


The main tasks of this project are as follows:

• trajectory planning to cover terrain

• perform feature-matching from stereo images

• point cloud from features generation

• a mesh of the ground surface generation


### Installation and Build

Ubuntu version:
```
Ubuntu 20.04 LTS 
```
Before building, you may need to install OpenCV and PCL.

Install OpenCV:
```
sudo apt update
sudo apt install libopencv-dev python3-opencv
```
Install PCL:
```
sudo apt install libpcl-dev
```
Now you can start to build. Clone the repository and cd to '../catkin_ws'. In a terminal, run:
```
git submodule update --init --recursive
```
```
catkin build
```

### Run the Simulation:

After building, you can start to run the code.

In '../catkin_ws', source the environment in terminal:
```
source devel/setup.bash
```
Launch the simulation:
```
roslaunch simulation simulation.launch
```

Now the drone starts to fly on predifined trajectory. In Rviz window, you will see, that the generated point cloud are merging. In a few minutes you are firstly expected to see this PCL viewer window, which shows two Meshs with RGB information generated from Greedy triangle and Poisson reconstruction algorithm. 

Then wait a few minutes, you are expected to see another PCL viewer window, which shows four meshs. On the upper part are two meshs without RGB color. On the lower side are two meshs with color information based on the height. The color change from blue to red according to the height.


### Demo
- 

### Architecture Overview and Interfaces
![image](https://github.com/TUM-AAS/autsys-projects-amg/blob/main/image/rosgraph.png)

### Reference

1. Mohsan, S.A.H., Othman, N.Q.H., Li, Y. et al. Unmanned aerial vehicles (UAVs): practical aspects, applications, open challenges, security issues, and future trends. Intel Serv Robotics 16, 109–137 (2023). https://doi.org/10.1007/s11370-022-00452-4
2. http://docs.ros.org/en/melodic/api/sensor_msgs/html/msg/CameraInfo.html
3. https://johnwlambert.github.io/stereo/
4. http://wiki.ros.org/stereoimageproc
5. http://wiki.ros.org/rviz (Accessed on Mar. 21, 2023)
6. https://diglib.eg.org/handle/10.2312/SGP.SGP06.061-070
7. https://pointclouds.org/documentation/tutorials/index.html
8. http://t.csdn.cn/YpuzY
9. http://t.csdn.cn/Dyq1a

