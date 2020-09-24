# Object-oriented programming in Python

Object-oriented programming (OOP) means that programs have a strong tendency of being organised around data, or objects, rather than functions and logic. That means a class represents the idea or concept behind something more tangible, like an actual object reasonably specific to your business. For example, when working on an education program, a class could be a student, teacher, or classroom.

With Python, it certainly can be used as a scripting language, it is designed as an object-oriented programming language.

### Prerequisites
Basic knowledge of Python programming is required. Watch the following YouTube videos to recap your Python skills:

**Basic Python 3 - Part 1**

[![Part 1](http://img.youtube.com/vi/Jw3h06aIHYk/0.jpg)](http://www.youtube.com/watch?v=Jw3h06aIHYk)

**Basic Python 3 - Part 2**

[![Part 1](http://img.youtube.com/vi/I_fpG3wrVaQ/0.jpg)](http://www.youtube.com/watch?v=I_fpG3wrVaQ)

### Topics
1. Classes and instances
2. Class variables
3. Class and static methods
4. Inheritance
5. Special methods

### 1. Classes and instances

```python
class Car:

    def __init__(self, maker, year):
        self.maker = maker
        self.year = year
        self.status = 'dirty'
    
    def clean():
        print('... cleaning the car!')
        self.status = 'clean'


my_car = Car('Honda', 2020)
print(my_car.maker)
print(f'The car is in {my_car.status} status')
my_car.clean()
print(f'The car is now in {my_car.status} status')
```

### 3. Class and static methods

```python
class iPhone:

    iPhone_list = ['8s', 'X', 'XS', '11']

    def __init__(self, model):
        self.model = model
    
    @classmethod
    def from_year(cls, year):
        return cls(iPhone.iPhone_list[int(year) - 2011])
    
    @staticmethod
    def newest_model():
        return iPhone.iPhone_list[len(iPhone.iPhone_list) - 1]
    
    def __repr__(self):
        return self.model


if __name__ == "__main__":
    a = iPhone('X')
    b = iPhone.from_year(2008)

    print("Newest model: " + iPhone.newest_model())
    print("a has " + str(a))
    print("b has " + str(b))
    print("a == b: " + str(a == b))
    print("a.model == b.model: " + str(a.model == b.model))
```
