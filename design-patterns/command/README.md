# Command Pattern Exercise

## Problem Description

You are working on a smart home system. The system includes various devices like lights, a garage door, and a stereo system. You need to create a universal remote control to interact with these devices.

Your task is to implement the Command Pattern to encapsulate each operation as an object which can be used by the remote control.

## Instructions

1. Define an interface (or an abstract class if the language doesn't support interfaces) `Command` with a method `execute`.

2. Implement concrete command classes `LightOnCommand`, `GarageDoorOpenCommand`, `StereoOnWithCDCommand` etc., that implement the `Command` interface. Each of these classes will need a receiver object (the device it controls) and implement the `execute` method to perform the operation on the receiver.

3. Implement a `RemoteControl` class with a method `set_command` to set a slot with a `Command`, and a method `button_was_pressed` to execute the `Command` in a particular slot.

4. In your main program, create an instance of `RemoteControl`, create command objects for each operation, assign these commands to slots in the remote control, and then simulate pressing the buttons to execute these commands.

## Tips

- You can use the concept of "invoker" and "receiver" while designing this pattern. The remote control is the invoker, and the devices are receivers.

## Expected Output

You should be able to assign commands to the remote control and execute them. For example:

```python
remote_control = RemoteControl()

light = Light()
garage_door = GarageDoor()
stereo = Stereo()

light_on = LightOnCommand(light)
garage_door_open = GarageDoorOpenCommand(garage_door)
stereo_on = StereoOnWithCDCommand(stereo)

remote_control.set_command(0, light_on)
remote_control.set_command(1, garage_door_open)
remote_control.set_command(2, stereo_on)

remote_control.button_was_pressed(0)
remote_control.button_was_pressed(1)
remote_control.button_was_pressed(2)
```
