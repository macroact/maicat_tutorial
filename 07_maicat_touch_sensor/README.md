# Maicat Tutorial
## [Only for Ubuntu] Touch Sensor

Maicat has three touch sensors, two on its head and one on its back.<br/>
The Education Version (EV), which this tutorial is geared towards, is by default set to randomly move its head and tail on every touch,<br/>
and to show the happy eye expression.<br/>
You can customize this to make a “meow” sound or perform other behaviors when you directly touch the robot in the designated areas.

- Top of the head
- Back of the head
- Back 

&nbsp;

### SSH Connection
To change the settings, you need to write your own source code.<br/>
In order to write and apply the code, you need to connect to Maicat's system, which is done using the SSH command.<br/>
Enter the command below in the terminal on your PC, with the hostname set to maibot + the last number of the UUID + .local.<br/>

```python
#input the SSH command then enter the password
ssh maicat@maibot.local
```

Alternatively, you can connect using the IP address confirmed in 1. [Network Settings and IP Address Verification](01_maicat_network/README.md).

```python
#input the SSH command then enter the password
ssh maicat@192.168.0.1 (maicat ip address)
```

&nbsp;

If the connection is successful, you will see a message asking you to enter a password.<br/>
Maicat's default password is "mai2019". Please enter all alphabets in lowercase.
After logging into the Maicat system, stop "maibot_interaction.service", which plays the role for the interaction.

```python
sudo systemctl stop maibot_interaction.service
```

&nbsp;

Then, it brings up the editing screen for the script where you can modify the touch response. 

```python
nano maicat_automatic/install/maibot_interaction/lib/python3.9/site-packages/boot/brain_ev_node.py
```

&nbsp;

The code below is the default setting for touch response. After modifying it to your liking, save it with ctrl+o --> enter and exit the editing screen with ctrl+x. 

```python
def _callback_touch(self, msg):
    if self._is_first_touch:
        subprocess.call(["sudo", "systemctl", "start", "maibot_gpt.service"])
        self._is_first_touch = False

    self._orders_teensy(4)
    self.default_head_vertical = round(random.uniform(self.servo_limit_head[0], self.servo_limit_head[1]), 2)
    self.default_head_tilt = round(random.uniform(self.servo_limit_head_side[0], self.servo_limit_head_side[1]), 2)
    self.default_tail = round(random.uniform(self.servo_limit_tail[0], self.servo_limit_tail[1]), 2)
    self._orders_servo([self.default_head_vertical, self.default_head_tilt, self.default_tail])
    time.sleep(0.4)
    self.default_head_vertical = round(random.uniform(self.servo_limit_head[0], self.servo_limit_head[1]), 2)
    self.default_head_tilt = round(random.uniform(self.servo_limit_head_side[0], self.servo_limit_head_side[1]), 2)
    self.default_tail = round(random.uniform(self.servo_limit_tail[0], self.servo_limit_tail[1]), 2)
    self._orders_servo([self.default_head_vertical, self.default_head_tilt, self.default_tail])
    self.default_head_vertical = round(random.uniform(self.servo_limit_head[0], self.servo_limit_head[1]), 2)
    self.default_head_tilt = round(random.uniform(self.servo_limit_head_side[0], self.servo_limit_head_side[1]), 2)
    self.default_tail = round(random.uniform(self.servo_limit_tail[0], self.servo_limit_tail[1]), 2)
    self._orders_servo([self.default_head_vertical, self.default_head_tilt, self.default_tail])
    self._orders_teensy(5)
```

&nbsp;

To see the changes, run 'maibot_interaction.service', wait about a minute, and then touch Maicat's head and back.

```python
sudo systemctl start maibot_interaction.service
```

&nbsp;

[Next - Maicat moving head and tail](../08_maicat_move_head_and_tail/README.md)
