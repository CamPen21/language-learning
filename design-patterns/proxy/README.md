# Proxy Pattern Exercise

## Problem Description

You're working on a database system. To debug issues, you want to log every database operation (like adding and removing records) without modifying the database code itself.

Your task is to implement the Proxy Pattern to create a logging proxy for the database access object.

## Instructions

1. Define a `Database` interface with methods `add_record` and `remove_record`.

2. Implement a `DatabaseImpl` class that implements the `Database` interface and performs operations on the database (for now, it can just print messages).

3. Implement a `DatabaseProxy` class that also implements the `Database` interface. It should delegate the calls to `add_record` and `remove_record` to an instance of `DatabaseImpl`, but also log these operations.

## Tips

- The `DatabaseProxy` should be initialized with an instance of `DatabaseImpl`.
- Make sure that the `DatabaseProxy` logs the operations before delegating the calls to the `DatabaseImpl`.

## Expected Output

You should be able to create a `DatabaseProxy`, perform operations on it, and see that these operations are logged. For example:

```python
database = DatabaseProxy(DatabaseImpl())

database.add_record("Record1")
database.remove_record("Record1")
```
