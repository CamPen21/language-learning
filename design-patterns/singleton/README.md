# Singleton Pattern Exercise

## Problem Description

Imagine you're designing a print spooler for an operating system. Since the print spooler handles a system resource (the printer), there should only ever be one instance of the spooler in the system to prevent conflicts.

Your task is to use the Singleton Pattern to ensure that there's only ever one instance of the `PrintSpooler` class.

## Instructions

1. Create a `PrintSpooler` class.
2. Implement it as a Singleton class, i.e., it should return the same instance whenever an instance of the class is requested.
3. The `PrintSpooler` class should have a `print` method that takes a document and outputs a message saying the document is printing.
4. In your main program, demonstrate that the `PrintSpooler` is indeed a singleton by trying to create two instances and showing that they are the same.

## Tips

- Use a class or static variable to store the instance.
- You will need to control access to the constructor, usually making it private, and create a public method to get the instance.

## Expected Output

You should be able to demonstrate that only one instance of `PrintSpooler` exists. For example:

```python
spooler1 = PrintSpooler.get_instance()
spooler2 = PrintSpooler.get_instance()

print(spooler1 is spooler2)

spooler1.print('Document1.txt')
spooler2.print('Document2.txt')
```
