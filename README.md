# Scan Matching Localization Project

## Dependencies
Before you practice the exercises in this repository, ensure that your development environment is configured with the following tools and dependencies:

- [CARLA simulator 0.9.9.4](https://github.com/carla-simulator/carla/releases/tag/0.9.9) 
- [NICE DCV Server](https://docs.aws.amazon.com/dcv/latest/adminguide/setting-up-installing-linux-prereq.html). This step will install Nvidia drivers along with CUDA libraries for the underlying Tesla T4 GPU
- C++ 
- Git
- [OpenCV](https://docs.opencv.org/4.x/d7/d9f/tutorial_linux_install.html)
- [CMake](https://askubuntu.com/questions/161104/how-do-i-install-make) and Make
- [VSCode](https://code.visualstudio.com/download), or a similar IDE
- [Eigen Library for C++](https://eigen.tuxfamily.org/index.php?title=Main_Page)
- [Point Cloud Library](https://pointclouds.org/downloads/)
- Python3 and Pip
- ROS


## Intall & Run
To begin with, clone the repository to your local development environment using the following commands:

```bash
git clone https://github.com/mose247/scan_matching_localization.git
cd nd0013_cd2693_Exercise_Starter_Code
```

Next, ensure that the **libcarla-install/** folder is present in your current working directory. The folder contains the static binaries built for the target VM workspace environment. If the folder is missing or corrupt, you can regenerate the files using the following command:

```bash
chmod +x make-libcarla-install.sh
./make-libcarla-install.sh
```

Compile the project using the following commands. 
```bash
cmake .
make
```

These steps will generate the `cloud_loc` executable. Open a new Terminal tab and execute the following command to start the simulator.

```bash
./run_carla.sh
```  

Open another Terminal tab and execute the following to run the project.
```bash
./cloud_loc 
```

If you encounter core dump on start up, just rerun and try again. Crash doesn't happen more than a couple of times. 
Next, to run the simulation follow the instructions in the specific [README](/Lesson_7_Project_Scan_Matching_Localization/c3-project/README.md). 

## Results
Localization using ICP scan matching over a 190m road segment.
![img](https://github.com/mose247/localization_exercises/blob/main/Lesson_7_Project_Scan_Matching_Localization/c3-project/img/ICP_results.png)
