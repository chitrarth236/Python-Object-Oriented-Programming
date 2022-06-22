## 3 Types of Methods in OOP Python
1. Instance Method
2. Static Method 
3. class Method 

### 1. Instance Method

  - Uses Instance variables inside the method
  - Uses self variable to point the current object
  - self is used to for instance variable manipulation inside Instance method
  - Accessible via object reference variable

### 2. Class Method

  - Uses static variables inside the method
  - @classmethod decorator is used to declare it
  - uses cls variable to point the current class
  - Accessible via classname or object reference

### 3. Static Method
  - No Instance or Static variable is used inside these method
  - @staticmethod decorator is used to declare it
  - Accessible via classname or object reference