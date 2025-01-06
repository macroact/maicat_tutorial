# Maicat Tutorial
## [Only for Ubuntu] Simulation Using Gazebo:

First, you'll need to install Gazebo for your version of Ubuntu.<br/>
https://gazebosim.org/docs/harmonic/install_ubuntu/ (For Ubuntu Jammy(22.04))

As described in the chapter [TOF Sensor](../05_maicat_tof_sensor/README.md) you need to install the packages for your PC.<br/>

&nbsp;

You can then run Maicat Gazebo on the same PC and test the behavior.<br/>
However, you'll need to open two terminal windows to run the two launch files<br/>
and each window must have the package's environment configured for the PC.

```python
cd maicat_pc (Package installation folder for pc)
source install/setup.bash
```

&nbsp;

(PC Terminal 1)
```python
ros2 launch maibot_gazebo maibot_gazebo.launch.py
```

(PC Terminal 2)
```python
ros2 launch maibot_navigation2 navigation.launch.py
```

&nbsp;

Launch Navigation:
- Select '2D Nav Goal' from the menu.
- Click and drag where you want Maicat to go and to determine the direction, and Maicat will start moving.
  
![maicat_nav2](https://github.com/macroact/maicat_tutorial/assets/106013071/90751657-4bc9-4f9e-9bb7-d88695391434)


[Next - Maicat slam](../11_maicat_slam/README.md)
