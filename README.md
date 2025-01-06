# Ruby Instance Variable Modification Bug

This repository demonstrates an uncommon bug in Ruby related to modifying instance variables through getter methods.  The example shows that directly assigning a value to the getter method does not modify the underlying instance variable. This can lead to unexpected behavior and difficult-to-debug issues if not understood.

## Bug Description
The `MyClass` class defines a getter method `value` for the instance variable `@value`. While you can modify `@value` directly using `instance_variable_set`, attempting to assign a new value via `my_object.value = 30` does not change the instance variable. The getter acts only as a read-only accessor in this case. 

## Solution
The solution demonstrates the correct way to modify instance variables; use setter methods or directly use `instance_variable_set`.