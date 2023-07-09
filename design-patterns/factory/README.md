# Factory Pattern Exercise

## Problem Description

Suppose you are working on a pet adoption application. Your application supports the adoption of different kinds of pets, such as dogs, cats, and rabbits.

Your task is to implement the Abstract Factory Pattern to create objects of different classes (Dog, Cat, Rabbit) based on the type of pet.

## Instructions

1. Define an abstract `Pet` class with a `speak` method that each type of pet will implement differently.

2. Create concrete `Dog`, `Cat`, and `Rabbit` classes that extend the `Pet` class and implement the `speak` method.

3. Define an abstract `PetFactory` class with a method `get_pet`.

4. Implement concrete `DogFactory`, `CatFactory`, and `RabbitFactory` classes that extend `PetFactory` and implement the `get_pet` method. Each factory should return an instance of its respective pet type.

5. In your main program, create an instance of each type of pet using the corresponding factory and call the `speak` method.

## Tips

- Make sure to have an appropriate string representation for each pet type.
- Do not forget to call the parent's constructor from the derived classes, if required.

## Expected Output

You should be able to create pets of different types and make them speak. For example:

```python
dog_factory = DogFactory()
dog = dog_factory.get_pet()
print(dog)
print(dog.speak())

cat_factory = CatFactory()
cat = cat_factory.get_pet()
print(cat)
print(cat.speak())

rabbit_factory = RabbitFactory()
rabbit = rabbit_factory.get_pet()
print(rabbit)
print(rabbit.speak())
```
