# Maicat Tutorial
# Maicat Move Leg and Controlling Maicat using your PC keyboard

```python
#Install xterm
sudo apt install xterm
```
```python
git clone https://github.com/macroact/maicat_pc.git
# run the following command
cd maicat_pc$
source install/setup.bash
ros2 launch maibot_teleop teleop.launch.py
```
Controlling Maicat using a PC is straightforward, much like driving a car. We utilize a set of 9 keys to direct Maicat's movements, each corresponding to different directions and actions:
```python
U: Turn left. Use this key when you need Maicat to change direction to the left.
I: Go straight. Press this to move Maicat forward in a straight line.
O: Turn right. This key makes Maicat turn to the right.
J: Move sideways to your left. This key shifts Maicat to the left without changing the direction it's facing, similar to a sidestep.
K: Stop. Press this key to make Maicat halt all movement immediately.
L: Move sideways to your right. Similar to 'J', but moves Maicat to the right.
M: Turn left while reversing. This command causes Maicat to reverse while simultaneously turning left, useful for backing out of tight spots.
, (comma): Reverse. This key moves Maicat straight backwards.
. (period): Turn right while reversing. This key works like 'M', but turns Maicat to the right while it reverses.
```
Video 3 (in progress)

[Next - Macat gazebo](../10_maicat_gazebo/README.md)
