# Camera-Intel-T265

Modification By: Cj-Heru05                                                                                                                              
Date: April 26, 2021

1. **Introduction**
The app should open a window divided into 4 viewports: top (top left viewport), front (bottom left viewport), side (bottom right viewport), and 3D (top right viewport). In each field of view, a 3D model of the camera and the corresponding 2D trajectory are displayed. In 3D view, you should be able to interact with the camera using your mouse, to rotate, zoom, and pan. Draw the device movement trajectory based on pose data. by using a device that supports intel camera pose stream (T265).
      ```
      1. Sequence of Images
      2. Ground Truth Data (pose)
      3. Calibration file (calib.txt)
      4. Timestamp (times.txt)
      ``` 

2. **How to install realsense2**
  - The following steps have been tested on Ubuntu 20.04 (Focal),
     ```
     $ sudo apt install libglfw3-dev libgl1-mesa-dev libglu1-mesa-dev libusb-1.0-0-dev
     
     $ mkdir -p ~/repos && cd ~/repos
 
     $ git clone https://github.com/IntelRealSense/librealsense

     $ mkdir -p librealsense/build && cd librealsense/build

     $ cmake .. -DFORCE_RSUSB_BACKEND=true -DCMAKE_BUILD_TYPE=release

     $ make -j(nproc)

     $ sudo make install
     ```
     
3. **How to used**
  - Follow these steps to run
  - Open your terminal by clicking Ctrl + Alt + T
     ```
     $ git clone https://github.com/Herusyahputra/Camera-Intel-T265.git
 
     $ cd Camera-Intel-T265

     $ realsense-viewer
     ```
     ![dof](https://user-images.githubusercontent.com/60929939/124540030-36eab200-de51-11eb-9b07-d8e504c02d26.png)

  - Open new terminal by clicking Ctrl + Alt + T
     ```
     $ cd trajectory
     ```
     ```
     $ rs-trajectory.cpp
     ```
     ![sensor](https://user-images.githubusercontent.com/60929939/124535660-13bc0480-de49-11eb-9152-7204af64de9c.png)

      
5. Result Pose Intel T265
   ![POSE](https://user-images.githubusercontent.com/60929939/142584803-2645c9d7-afce-405b-a46a-c452591a4d32.png)

7. **Refereness**

  - Install [realsense2](https://roboticslab-uc3m.github.io/installation-guides/install-realsense2.html) 
  - Intel [Librealsense](https://github.com/IntelRealSense/librealsense)
