# Polymorphism

## Poly means many. Morphs means forms.
## Polymorphism means 'Many Forms'.

- 1. Duck Typing Philosophy of Python
- 2. Overloading 
    - 1. Operator Overloading 
        - Operator overloading means the same operator can be used for multiple purposes. Python supports operator overloading.
        - Magic methods are used to implement it.
    - 2. Method Overloading 
        - If Multiple methods having same name but different type of arguments/return type, then these methods are said to be overloaded methods. 
        - But in Python Method overloading is not possible. If we are declaring multiple methods with same name and different number of arguments then Python will always consider only last method in the order.
        - We can handle method overloading till some point with default arguments or with variable number of argument methods. But it won't be a proper method overloading(Kinda hacky way).
    - 3. Constructor Overloading
        - Same as the method overloading, the constructor overloading is not possible in Python. If we define multiple constructors then the last constructor will be considered.
- 3. Overriding 
    - 1. Method overriding
    - 2. constructor overriding

    - Through inheritance, the methods/constructor of the parent class is directly available to the child class. Moreover, the child class can also modify the inherited methods/constructor implementation based on requirements. It is called overriding.
    ```
    class P:
        def m1(self): 
        print("Parent class method")

    class C(P):
        def m1(self):
        print("Child class method") 
    
    c=C()
    c.m1() # O/P : Parent class method
    c.m1() # O/P : Child class method
    #Here, you can see the same name but different implementations
    ```

    - To call Parent class methods and constructor from the child class members super keyword is used. check out the calling methods and constructor via the super keyword section of [this guide](https://github.com/chitrarth236/Python-Object-Oriented-Programming/tree/main/inheritance).
