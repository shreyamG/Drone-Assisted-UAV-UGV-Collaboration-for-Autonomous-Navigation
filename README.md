# Drone-Assisted UAV-UGV Collaboration for Autonomous Navigation in Snow-Covered Terrain
A novel UAV-UGV collaborative navigation framework integration of a custom-trained U-Net model for real-time road segmentation with a modified architecture that includes a novel data augmentation technique, which utilizes synthetic snow images to improve the model’s ability to segment roads accurately in varying snow conditions.

## Installation Instructions

- In the `src` folder of your catkin workspace clone the repository.
- Run `catkin build` inside your workspace directory.
- Install dependencies
  ```
  rosdep install --from-paths src --ignore-src -r -y
  ```
- Run below commands for the Gazebo simulation:
  - World 1:
    ```
    roslaunch uav_ugv uav_ugv_world1.launch
    ```
  - World 2:
    ```
    roslaunch uav_ugv uav_ugv_world2.launch
    ```
  - For world 3
    ```
    roslaunch uav_ugv uav_ugv_world3.launch
    ```
- In another terminal to run Ardupilot:
  ```
  sim_vehicle.py -v ArduCopter -f gazebo-iris --console
  ```
