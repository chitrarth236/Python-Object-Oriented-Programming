## 3 Types of Variables in OOP Python
1. Instance Variable (Object Level)
2. Static Variable (Class Level)
3. Local Varibale (Method Level)


### 1. Instance Variable

- ####  How to Declare:
  - Using object variable (Outside the class)
  - Using self (Inside the constructor and instance method)

- #### How to Access:
  - Using object variable (Outside the class)
  - Using self (Inside the constructor and instance method)

- #### How to Delete:
  - Using del keyword with object variable, Outside the class(ex. del objectname.variablename)
  - Using del keywork with self within a class (ex. del self.variablename)
  
### 2. Static Variable

- ####  How to Declare:
  - Directly within class but outside on any method and constructor
  - Using class name within in any method(instance, static, class)/constructor using class name
  - Using cls variable in class method
  
- #### How to Access:
  - Using self or class name inside instance methods/constructor
  - Using cls variable or class name inside class and static methods
  - Using object variable or class name outside the class

- #### How to Modify:
  - Using class name inside or outside the class
  - Using cls variable in class method
  
- #### How to Delete:
  - Using del keyword with class name, Outside the class(ex. del classname.variablename)
  - Using del keyword with cls var inside a class method(ex. del cls.variablename)
  
### 3. Local Variable
	
  - Local variables are created and used inside the method
  - they are not accessible outside the method
