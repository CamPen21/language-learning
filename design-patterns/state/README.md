# State Pattern Exercise

## Problem Description

Imagine you're designing a simple game. In this game, characters can be in different states (e.g., standing, running, jumping, ducking). Each state has different behaviors for the character.

Your task is to implement the State Pattern to encapsulate the behavior associated with each state of the character.

## Instructions

1. Define a `CharacterState` interface (or an abstract class) with methods for each action a character can take (e.g., `move`, `jump`, `duck`).

2. Implement concrete `StandingState`, `RunningState`, `JumpingState`, and `DuckingState` classes that implement the `CharacterState` interface. Each of these states should alter the character's behavior appropriately.

3. Implement a `GameCharacter` class with a `state` property and methods for each action a character can take (e.g., `move`, `jump`, `duck`). Each action should delegate to the current state.

4. Allow the `GameCharacter` to transition between states when certain actions are taken.

## Tips

- Remember to change the state of the character appropriately when actions are taken. For example, if a character jumps while standing, their new state should be jumping.

## Expected Output

You should be able to create a `GameCharacter` and have it change states and behavior. For example:

```python
character = GameCharacter()
character.move()
character.jump()

character.state = DuckingState()
character.move()
character.jump()
```
