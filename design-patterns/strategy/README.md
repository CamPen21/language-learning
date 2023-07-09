# Strategy Pattern Exercise

## Problem Description

You are working on a vehicle simulation program. The program should support different types of vehicles, and each vehicle can have different methods for moving, like driving, flying, or sailing.

Your task is to implement the Strategy Pattern to encapsulate the behavior of these vehicles.

## Instructions

1. Define an abstract class `Vehicle` with the following attributes: `name` and `move_strategy`. The `move_strategy` should be a method that will be overridden by the actual vehicle type (Car, Airplane, Boat).

2. Implement a `move` method in the `Vehicle` class that calls the `move_strategy`.

3. Create three classes `Car`, `Airplane`, and `Boat`, each inheriting from the `Vehicle` class. For each of these classes, override the `move_strategy` to print a unique message, like "Driving on the road", "Flying in the sky", or "Sailing on the sea".

4. Create a few instances of each type of vehicle and call their `move` method to demonstrate your solution.

## Tips

- Make sure each vehicle class has a proper string representation method for printing.
- Do not forget to call the parent's constructor from the derived classes.

## Expected Output

You should be able to call the `move` method on any type of vehicle and get the expected output. For example:

```python
car = Car("Toyota")
print(car)
car.move()

airplane = Airplane("Boeing")
print(airplane)
airplane.move()

boat = Boat("Titanic")
print(boat)
boat.move()
```
