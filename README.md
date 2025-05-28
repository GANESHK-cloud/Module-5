# Experiment No: 5a-Employee Class with Parameterized Constructor

## AIM  
To create a Python class `employee` with parameterized constructors with the parameters as `id` and `name`, and print the details of the employee using the `display(self)` method.

---

## ALGORITHM  
1. Begin the program.  
2. Define a class `employee` with a parameterized constructor that takes `id` and `name` as arguments.
3. Define a method `disp()` to display the employee's details.
4. Read input values for `id` and `name` from the user.
5. Create an instance of the `employee` class.
6. Call the `disp()` method to display the employee details.
7. Terminate the program.

---

## 🧾 PROGRAM

```python
class employee:
    def __init__(self, id, name):
        self.id = id
        self.name = name
    
    def disp(self):
        print(f"Hello my id is : {self.id}")
        print(f"My name is : {self.name}")

id = input()
name = input()
e = employee(id, name)
e.disp()

```

### OUTPUT
![image](https://github.com/user-attachments/assets/8240db55-9930-4f09-85cc-ad108de592f9)

### RESULT
Thus, the Python program to create an employee class with parameterized constructor and display employee details has been implemented and executed successfully.


# Experiment No: 5b-Vehicle Class with Constructor and Destructor

## AIM  
To create a Python class `Vehicle` that has a constructor (`__init__`) and a destructor (`__del__`). We will create an instance of the class and delete it right after.

---

## ALGORITHM  
1. Begin the program.  
2. Define a class `vehicle` with the constructor `__init__(self)` to print "Vehicle created." when an object is instantiated.
3. Define a destructor `__del__(self)` to print "Destructor called, vehicle deleted." when the object is deleted.
4. Create an instance of the `vehicle` class.
5. The destructor will be automatically called when the object goes out of scope or is explicitly deleted.
6. Terminate the program.

---

## 🧾 PROGRAM

```python
class vehicle:
    def __init__(self):
        print("Vehicle created.")
    
    def __del__(self):
        print("Destructor called, vehicle deleted.")

v = vehicle()

```

### OUTPUT
![image](https://github.com/user-attachments/assets/b2d98b07-a507-4788-ad43-67abc83800b4)

### RESULT
Thus, the Python program to create a vehicle class with a constructor and destructor has been implemented and executed successfully.



# Experiment No: 5c–Add, Subtraction, and Division Using Multiple Inheritance

## AIM  
To create a Python program that calculates the addition, subtraction, and division using multiple inheritance.

---

## ALGORITHM  
1. Define class `c1` with a method `add(self, a, b)` to return the sum of `a` and `b`.
2. Define class `c2` with a method `sub(self, a, b)` to return the difference between `a` and `b`.
3. Define class `divi` that inherits from both `c1` and `c2`, and add a method `div(self, a, b)` to return the division result of `a` and `b`.
4. Take user input for `a` and `b`.
5. Instantiate the class `divi`.
6. Call the `add()`, `sub()`, and `div()` methods to perform the respective operations.
7. Display the results.
8. Terminate the program.

---

## 🧾 PROGRAM

```python
class c1:  
    def add(self, a, b):  
        return a + b  

class c2:  
    def sub(self, a, b):  
        return a - b  

class divi(c1, c2):
    def div(self, a, b):  
        return float(a / b)  

a = int(input())
b = int(input())
d = divi()  
print(d.add(a, b))  
print(d.sub(a, b))  
print(d.div(a, b))

```

### OUTPUT
![image](https://github.com/user-attachments/assets/1deac0a4-857c-4912-b075-be4b93f78590)


### RESULT
Thus, the Python program to perform addition, subtraction, and division using multiple inheritance has been implemented and executed successfully.


# Experiment No: 5d – Display Person Details Using Multilevel Inheritance

## AIM  
To write a Python program to get the name, age, and ID of a person and display the details using multilevel inheritance.

---

## ALGORITHM  
1. Define the base class `work` with a constructor to initialize the `name`.
2. Define a derived class `Employee` inheriting from `work`, with an additional parameter `age`.
3. Define another derived class `Salary` inheriting from `Employee`, with an additional parameter `salary/id`.
4. Include a `disp()` method in `Salary` to print the name, age, and salary/id.
5. Get user input for name, age, and id.
6. Create an instance of the `Salary` class.
7. Call the `disp()` method to display the result.
8. Terminate the program.

---

## 🧾 PROGRAM

```python
class work:
    def __init__(self, name):
        self.name = name

class Employee(work):
    def __init__(self, name, age):
        super().__init__(name)
        self.age = age

class Salary(Employee):
    def __init__(self, name, age, salary):
        super().__init__(name, age)
        self.salary = salary

    def disp(self):
        print(f"{self.name} {self.age} {self.salary}")

name = input()
age = int(input())
salary = int(input())

person = Salary(name, age, salary)
person.disp()

```

### OUTPUT
![image](https://github.com/user-attachments/assets/eb76b846-239d-4f45-82b7-f9faf3656eff)

### RESULT
Thus, the Python program to display the details of a person using multilevel inheritance has been executed successfully.



# Experiment No: 5e – SEB- Check Exam Eligibility Using Inheritance

## AIM  
To write a Python program to get the name, attendance, and ID of a student and check their eligibility for the exam using multiple inheritance.

---

## ALGORITHM  
1. Define a base class `Person` with attributes for name and age.
2. Define a base class `Student` with an attribute for attendance percentage.
3. Create a derived class `Resident` inheriting from both `Person` and `Student`.
4. Use constructors in each class to initialize the attributes.
5. Create methods to display name and age.
6. Check if attendance is greater than 75 to determine eligibility.
7. Print “Eligible for Exam” or “Not Eligible for Exam” accordingly.

---

## 🧾 PROGRAM

```python
class Person:  
    def __init__(self, personName, personAge):  
        self.name = personName  
        self.age = personAge  

    def showName(self):
        print(self.name)

    def showAge(self):  
        print(self.age) 
        
class Student:
    def __init__(self, studentpercent):  
        self.studentpercent = studentpercent  
  
    def getpercent(self):  
        return self.studentpercent  
  
class Resident(Person, Student): 
    def __init__(self, name, age, percent):
        Person.__init__(self, name, age)
        Student.__init__(self, percent)

name = input()
age = int(input())
percent = int(input())

resident1 = Resident(name, age, percent)  
resident1.showName()  
resident1.showAge()  

if resident1.getpercent() > 75:
    print("Eligible for Exam")
else:
    print("Not Eligible for Exam")

```

### OUTPUT  
![image](https://github.com/user-attachments/assets/51e86e78-1a01-454a-9669-a09ea2a36c98)

### RESULT
Thus, the Python program to check exam eligibility using multiple inheritance has been executed successfully.
