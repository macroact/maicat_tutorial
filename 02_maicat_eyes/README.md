# Maicat Tutorial
## Change the eyes of your Maicat 

You can change the color and the shape of Maicat's eyes to express different emotions.
The display change numbers are 0 through 9.
The color numbers are as follows

    0: yellow
    1: blue
    2: pink
    
To change the eyes' shape use the following numbers below.
    
    3: Normal
    4: Happy
    5: Surprised
    6: Angry
    7: Sad
    8: Sleepy
    9: Asleep

&nbsp;
### [For Block-Coding]
- 'Start'
To execute commands with the block-coding you must placed them inside the 'Start'-block.
With your mouse drag the 'Start'-block into the execution screen.

<img src="https://github.com/user-attachments/assets/6c4e5446-ddc2-4020-9960-7e9ed97bc692" alt="bc-start" width="250">

- 'Eye Style'
Choose your favorite eye type and drag it into the 'Start'-Block.

<img src="https://github.com/user-attachments/assets/2615d183-350c-4a31-810a-e1d10cb0e13f" alt="bc_eye" width="250"/>

- Trash-Icon

Drag blocks you no longer use with your mouse and drop them in the trash can icon.

![trash](https://github.com/user-attachments/assets/796d9e0e-b132-4d5f-b425-740ae434a23a)    

- Center, Zoom In, Zoom Out

Used for centering the screen or zooming in and out.

![zoom](https://github.com/user-attachments/assets/0fffbb61-505e-47f5-8591-8a29ce5e59d5)

&nbsp;
### [For Ubuntu]
On a PC with ROS2 installed, enter the following command to change the color and shape to your desired one.

```python
ros2 topic pub serial number(UUID)/control_teensy std_msgs/Int64 "data: insert eye number you want to change"
```


&nbsp;
<br/>
![Maicat_eyes_expressions_emotion-ezgif com-optimize](https://github.com/macroact/maicat_tutorial/assets/106013071/98a80e0c-b105-490c-bc51-b6e511328f80)

&nbsp;
[Next - The mouth of maicat](../03_maicat_mouth/README.md)
