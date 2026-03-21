## Week 8 — Object-Oriented Programming 
OOP is a programming paradigm for organizing code around real-world entities
- `class` - blueprint/template for a custom data type you invent
- `object` - one specific thing created from that blueprint
- `__init__(self, ...)`	- When you create an object, initializes its values
- `__str__(self)`	- When you print() or str() the object, returns a readable string
- `__add__(self, other)` - When you use + between two objects of this class
- `instance variable`	- variable stored inside a specific object (self.name)
- `instance method`	- function inside a class that operates on a specific object, always takes self
- `class variable`	- variable shared by ALL objects of the class (no self)
- `class metho`d	- function that belongs to the class itself, not a specific object, takes cls
- `constructor`	-  call that creates an object, e.g. Student("Harry", "Gryffindor")

### Properties
Prevent invalid values being set on an attribute after object creation
`@property` = getter, when you read the attribute
```
@property
def house(self):
    return self._house
```
`@name.setter` = setter, when you assign to the attribute
By convention, the underlying instance variable uses a leading underscore: _house
In `__init__`, use `self.house` = house (no underscore) so the setter runs and validates on creation too

### Inheritance
A subclass inherits all attributes and methods from its superclass (parent)
- `super().__init__()` - to call the parent's init from the child's init, avoids copy-pasting shared logic into every class
- `__add__ `- define to make + work between two objects of your class
- `self` = left operand
- `other` = right operand
- `raise ValueError("message")` - signal bad input inside a class
