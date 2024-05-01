# Maicat Tutorial
## Removing seal from the battery.
      
First, to prepare the robot for use, remove the safety seal from the battery. Then, press the power button to turn on Maicat, as illustrated in the picture above. You should see light activate indicating that the robot, Maicat, is powering on.

(video 1)
Picture1 Maicat seal (in progress)
Picture2 Maicat power button (in progress)


When working with the Maicat, we recommend using Ros2 Humble, which is a long-term support (LTS) version, compatible with Ubuntu 22.04 LTS.

Ubuntu 22.04 LTS (jammy) (install)
Download ling https://ubuntu.com/download/desktop 

ROS2 Humble
Use the following link to install ROS2 Humble https://docs.ros.org/en/humble/Installation/Alternatives/Ubuntu-Development-Setup.html

Installing ROS2 Humble

```python
sudo apt update
sudo apt upgrade
```
On the terminal:

```python
locale # check for UTF-8
```

If you don't have US.UTF-8 install bellow lines

```python
sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8

locale  # verify settings
```

Note* Make sure to setup sources so that Ros2 can work.

```python
sudo apt install software-properties-common
sudo add-apt-repository universe
```

Now add the ROS 2 GPG key with apt.

```python
sudo apt update && sudo apt install curl -y
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg
```

Lastly run this to add the repository to your sources list.

```python
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null

sudo apt update&sudo apt upgrade
```

Now install ROS2 After the above.

```python
sudo apt install ros-humble-desktop
```

Setting up Network:

Pairing
After logging in, the user will be prompted to either establish a Bluetooth connection with an existing Maicat or to set up a new connection. If an option is selected, the app will scan for nearby Maicat. Choose one of the scanned Maicat and attempt to connect.
Wi-Fi Settings
Search for networks that Maicat can connect to. Select your desired network from the list of available options, enter the correct password for your network, and Maicat will connect to the selected network.

Video 2.


Controlling Maicat using your PC keyboard

Controlling Maicat using a PC is straightforward, much like driving a car. We utilize a set of 9 keys to direct Maicat's movements, each corresponding to different directions and actions:
U: Turn left. Use this key when you need Maicat to change direction to the left.
I: Go straight. Press this to move Maicat forward in a straight line.
O: Turn right. This key makes Maicat turn to the right.
J: Move sideways to your left. This key shifts Maicat to the left without changing the direction it's facing, similar to a sidestep.
K: Stop. Press this key to make Maicat halt all movement immediately.
L: Move sideways to your right. Similar to 'J', but moves Maicat to the right.
M: Turn left while reversing. This command causes Maicat to reverse while simultaneously turning left, useful for backing out of tight spots.
, (comma): Reverse. This key moves Maicat straight backwards.
. (period): Turn right while reversing. This key works like 'M', but turns Maicat to the right while it reverses.

Video 3 (in progress)


Controlling robot through WiFi with ROS

One of Maicat's features is that users can customize the color and style of its eyes. There are seven eye styles available. To change the eye style, users can simply enter the command in the terminal as shown below.

    3: Normal
    4: Happy
    5: Surprise
    6: Angry
    7: Sad
    8: Sleepy
    9: Sleep

ON your PC terminal run the below command.

```python
ros2 topic pub teensy/command std_msgs/Int32 "data: number of the shape of eye you need" 
```

Video 4 (in process)


Robot control: Move the Mouth (this part i need to ask 대표님 because the users will use PC version)

To control the movement of Maicat you need to start the Ros2  workspace .
First run maicat
```python
ros2 launch maibot_bringup maibot.launch.py)
```
Second on the PC terminal run the below command:

```python
ros2 topic pub teensy/command std_msgs/Int32 "data: 30/33"
```

30->Opening the mouth.
33->Closing the mouth.

(video 5 done)

Robot control: Mic meow sound ()
In progress

Sensor Control (Camera) Streaming
In progress
