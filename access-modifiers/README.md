### By default every member in python class is public.

### Protected attributes can be accessed within the class and in child classes(from outside of the class). We can specify an attribute as protected by prefexing with _ symbol.

example: _name='Chitrarth'

Using single underscore _ is a convention, so when you see an attribute or method starting with one underscore, consider that the developer didn't expect it to be part of public API. Also when executing from module import * Python interpreter doesn't import names starting with _, though there're ways to modify this behavior.

### private attributes can be accessed only within the class.i.e from outside of the class we cannot access. We can declare a variable as private explicitly by prefexing with 2 underscore symbols.

example: __ClientID=23

Using double underscore __ is not just a convention, it leads to "name-mangling" by interpreter(adding class name in front of attribute)

### In Python, mangling is used for class attributes that one does not want subclasses to use, which are designated as such by giving them a name with two or more leading underscores and no more than one trailing underscore.

class A():
    def __private_method():
        print("Private member")

it will make "_A__private_method" property. You won't be able to access "__private_method" directly as defined, though you still will be able to get to it knowing how names are composed by using _"_A__private_method()" in subclasses for example or in module:

A.private_method() will give you an error.

A._A__private_method() will print "Private member".

### One good article : [here]https://medium.com/analytics-vidhya/python-name-mangling-and-how-to-use-underscores-e67b529f744f
