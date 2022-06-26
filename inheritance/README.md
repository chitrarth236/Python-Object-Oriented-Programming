## Inheritance in Python

### Types of Inheritance in Python
  - Single Inheritance
  - Multi Level Inheritance
  - Hierarchical Inheritance
  - Multiple Inheritance (Yes, Python supports multiple inheritance, using **MRO** and **C3** algorithm)
  - Hybrid Inheritance

### example:
```Python
  class P:
    def m1(self): 
      print("Parent class method")

  class C(P):
    def m2(self):
      print("Child class method") 
  
  c=C()
  c.m1() # O/P : Parent class method
  c.m2() # O/P : Child class method

```

### super() method

  - The built-in super() method is used to call the super class's constructors, variables and methods from the child class.

  #### Calling the constructor using super():

    ```python
    class Employee:
      def __init__(self, name, salary):
        self.name = name
        self.salary = salary

    class SDE1(Employee):
      def __init__(self, name, salary, department):
        super().__init__(name, salary)  # Calling the parent class'es constructor
        #another way to do it is: Employee.__init__(self, name, salary) but super() is more maintainable
        self.department = department
    ```

  #### Calling the method using super():

   - Using super(), from the child class's constructor and instance method, we can access the parent class instance method, static method and class method.
   - similar to calling the constructor, using syntax:
    ```python 
     super().method_name()
    ```
   - Using ```super().method_name()``` in the child class's class method, the parent's instance method and constructor are not accessible(only but parent's static and class methods are accessible). 
      - There is one indirect method to achieve this.

   - To call parent's static method in child's static methods, only indirect method can be used.

      ```python 
        class A:
          @staticmethod
          def m1():
            print('Parent static method') 
          
        class B(A):
          @staticmethod 
          def m2(): 
            super(B,B).m1()  # syntax: super(class_name, class_name).static_method_name()
          
        B.m2() # O/P : Parent static method
      ```

  #### Calling the variables using super():

   - using super() parent's instance variables are not accessible(they are accessible using "self.variable_name").
   - parent's static variables are accessible using super().

  #### Using super() to call perticular class's methods
   - Two ways:
      - Kclass.method1(self)  - It will call Kclass's method1() method.
      - super(Kclass,self).method1() It will call method1() method of super class of Kclass.
