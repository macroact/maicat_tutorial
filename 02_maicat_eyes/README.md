# Maicat Tutorial
## Change the eyes of maicat

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
# You will see the change of eyes color and eye style
```

Video (in process)

[Next - The mouth of maicat](../03_maicat_mouth/README.md)
