# Abstract classes, methods and interfaces

### Abstract Methods
- In Python abstract methods are defined using @abstractmethod decorator. It is placed before the method defination.
- The @abstractmethod decorator is available inside the 'abc'(abstract base class) module. Thus, before using it you must import 'from abc import *' 
- Child classes are responsible to provide the implementation of the abstract methods to create the object..

### Abstract Class
- To declare an abstract class in python, ABC class from the abc module is inherited.
- Abstract class can have zero or more abstract methods.
- Abstract class can also have normal methods.
- If the Abstract class have atleast one abstract then the object creation of the abstract class is not possible. It is possible in any other cases(i.e abstract class with no abstract methods or normal class with abstract methods)


```python
from abc import * 

class Person(ABC):
	@abtractmethod
	def commute(self):
		pass
```

### Interface
- Similar to Abstract class, but only contains abstract methods.
- the syntax for interface is same as abstract class, but only contains the abstract methods.