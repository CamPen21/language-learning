# Decorator Pattern Exercise

## Problem Description

Imagine you're designing a system for a coffee shop. This coffee shop sells different kinds of beverages like Espresso, Dark Roast, Decaf, and House Blend. Customers can also add various condiments to their beverages, like milk, soy, mocha, and whipped cream. Each condiment adds to the cost of the beverage.

Your task is to design a system using the Decorator Pattern where you can calculate the cost of any combination of beverage and condiments.

## Instructions

1. Create an abstract `Beverage` class. This class should have a `description` instance variable and two methods: `get_description` and `cost`.

2. Create concrete classes like `Espresso`, `DarkRoast`, `Decaf`, `HouseBlend` etc., that extend the `Beverage` class. The `cost` method for each class should return the cost of that specific beverage.

3. Create an abstract `CondimentDecorator` class that extends the `Beverage` class.

4. Create concrete condiment classes like `Milk`, `Soy`, `Mocha`, `WhippedCream` etc., that extend the `CondimentDecorator` class. Each of these classes should add its own cost to the beverage cost.

5. In your main program, allow creating a beverage and then adding condiments to it. The system should be able to correctly calculate the cost of the beverage with the added condiments.

## Tips

- Remember to call the base class's constructor and methods where necessary.
- You can assume that the cost of each item is known and constant.

## Expected Output

You should be able to create a beverage, add condiments, and calculate the total cost. For example:

```python
beverage = Espresso()
beverage = Mocha(beverage)
beverage = Whip(beverage)
print(beverage.get_description() + " $" + str(beverage.cost()))
```
