#### **GitHub Repository**: [LP_Virtual_Override_New](https://github.com/WCramRTC/LP_Virtual_Override_New)

## Required Lecture Video
[![IMAGE_ALT](https://img.youtube.com/vi/YY6Ve8n7lYA/0.jpg)](https://youtu.be/YY6Ve8n7lYA?si=IpQupGoWKuR2-1JT)

#### **GitHub Notes**: [Prog_124_S23_L5_Virtual_Override_New](https://github.com/WCramRTC/Prog_124_S23_L5_Virtual_Override_New)

Timestamps:
- [00:00:00 Start of Lecture](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=0s)
- [00:20:06 Defining what Vehicles are](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=1206s)
- [00:34:48 First Class: Vehicle](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=2088s)
- [00:41:30 Testing Our Vehicle Class](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=2490s)
- [00:46:16 Second Class: Land](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=2776s)
- [00:50:59 Key Concept: Virtual and Override Keyword](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=3059s)
- [00:57:55 Testing our Virtual and Override Methods](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=3475s)
- [00:59:09 Third Class: Sea and Refactoring our code](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=3549s)
- [01:13:44 Fourth Class: Train](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=4424s)
- [01:17:04 Fifth Class: Fork Lift](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=4624s)
- [01:28:58 Key Concept: New Keyword](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=5338s)
- [01:36:04 Example Two: Account, Bank Account, Checking Account](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=5764s)

You can click on the links to directly access the corresponding timestamps in the video.

---
### Goal

The goal of this documentation is to understand the following concepts in C#:

### **`virtual`**
- Indicates that a method or property in a base class can be overridden in derived classes.
- Enables polymorphism, allowing derived classes to provide custom implementations while adhering to the same method signature.

### **`override`**
- Used in a derived class to provide a new implementation for a method or property that was declared as virtual or abstract in the base class.
- The overriding method or property must have the same name, return type, and parameters as the base class member.
- Enables the replacement of the default behavior of the base class method with a custom implementation in the derived class.

### **`new`**
- Used to hide a base class member in a derived class when there is a naming conflict.
- Introduces a new member in the derived class with the same name, but it is not related to the base class member.
- Does not participate in polymorphism and can lead to potential confusion when working with derived classes.

Understanding these concepts is essential for effective use of inheritance and polymorphism in C# and for designing flexible and maintainable object-oriented code.

---
## Requirements

- Create a new project with the name of LP_Virtual_Override_New_YourName
- Comment your name at the top of the project
- Make sure your code compiles properly
- Submit your project as a git hub repository by pasting the repository link in canvas
- Answer the following questions in the README.md file in your project 
	- ( this is created when you selected [] Add README.md when you make your github repo)

	 1. **What is the purpose of the `virtual` keyword in C# and how does it work in the context of inheritance?**
	2. **Can you explain the difference between `override` and `new` keywords when used in derived classes in C#?**
	3. **How does the `override` keyword in C# affect method resolution at runtime?**
	4. **In what scenario would you use the `new` keyword in C# to hide a member of the base class?**
	5. **What happens if a derived class in C# overrides a `virtual` method from the base class without using the `override` keyword?**    
	6. **Can a `virtual` method in a base class in C# be overridden in multiple levels of derived classes? How does this affect the method behavior?**

- Create the following classes ( created in the lecture )

    1. **Vehicle (Base Class)**
        - Fields:
            - `ConsoleColor _backgroundColor`
            - `int _capacity`
            - `int _fuelCapacity`
            - `int _maxSpeed`
        - Methods:
            - `virtual void Accelerate()`

    2. **Land (Derived from Vehicle)**
        - Fields:
            - `int _numOfWheels`
        - Methods:
            - `override void Accelerate()`

    3. **Sea (Derived from Vehicle)**
        - Fields:
            - `double _displacement`
        - Methods:
            - `override void Accelerate()`

    4. **Train (Derived from Land)**
        - Fields:
            - `int _numOfCars`
        - Methods:
            - `override void Accelerate()`

    5. **Forklift (Derived from Land)**
        - Fields:
            - `int _weightCapacity`
        - Methods:
            - `override void Accelerate()`: Outputs "We are on the construction site."
            - `void RaiseForkLift()`: Outputs "The forklift is raised"

 - Test your code by creating instances of each class and calling their accelerate methods.
	 - Example
	 ```csharp            
		   Vehicle vehicle = new Vehicle(ConsoleColor.Green, 4, 12, 95);
            Land car = new Land(ConsoleColor.DarkMagenta, 8, 18, 85, 4);
            Sea sea = new Sea(ConsoleColor.DarkGray, 16, 30, 60, 40);
            Train train = new Train(ConsoleColor.Cyan, 100, 8, 55, 16, 100);

            Forklift forklift = new Forklift(ConsoleColor.DarkCyan, 2, 10, 15, 3);

            vehicle.Accelerate();
            car.Accelerate();
            sea.Accelerate();
            train.Accelerate();
            forklift.Accelerate();
            forklift.RaiseForkLift();
		```

**Extra Practice and Extra Credit :**
	- Build the Account, BankAccount, and Checking Account class from the last quarter of the lecture
	- Test the code

---
## Class Diagrams

Based on the code for the classes `Forklift`, `Land`, `Sea`, `Train`, and `Vehicle`, here is a class diagram that illustrates their relationships, methods, and fields:

### Class Diagram

- [00:20:06 Defining what Vehicles are](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=1206s)
- [00:34:48 First Class: Vehicle](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=2088s)
- [00:41:30 Testing Our Vehicle Class](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=2490s)

1. **Vehicle (Base Class)**
   - Fields: 
     - `protected ConsoleColor _color`
     - `int _capacity`
     - `int _fuelCapacity`
     - `int _maxSpeed`
     - `protected ConsoleColor _backgroundColor`
   - Constructor: `Vehicle(ConsoleColor color, int capacity, int fuelCapacity, int maxSpeed)`
   - Methods: 
     - `virtual void Accelerate()`

- [00:46:16 Second Class: Land](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=2776s)
- [00:50:59 Key Concept: Virtual and Override Keyword](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=3059s)
- [00:57:55 Testing our Virtual and Override Methods](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=3475s)

2. **Land (Derived from Vehicle)**
   - Fields: `int _numOfWheels`
   - Constructor: `Land(ConsoleColor color, int capacity, int fuelCapacity, int maxSpeed, int numOfWheels)`
   - Methods: `override void Accelerate()`

- [00:59:09 Third Class: Sea and Refactoring our code](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=3549s)


3. **Sea (Derived from Vehicle)**
   - Fields: `double _displacement`
   - Constructor: `Sea(ConsoleColor color, int capacity, int fuelCapacity, int maxSpeed, double displacement)`
   - Methods: `override void Accelerate()`

- [01:13:44 Fourth Class: Train](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=4424s)

4. **Train (Derived from Land)**
   - Fields: `int _numOfCars`
   - Constructor: `Train(ConsoleColor color, int capacity, int fuelCapacity, int maxSpeed, int numOfWheels, int numOfCars)`
   - Methods: `override void Accelerate()`

- [01:17:04 Fifth Class: Fork Lift](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=4624s)
- [01:28:58 Key Concept: New Keyword](https://www.youtube.com/watch?v=YY6Ve8n7lYA&t=5338s)
- 
1. **Forklift (Derived from Land)**
   - Fields: `int _weightCapacity`
   - Constructor: `Forklift(ConsoleColor color, int capacity, int fuelCapacity, int maxSpeed, int numOfWheels)`
   - Methods: 
     - `override void Accelerate()`
     - `void RaiseForkLift()`

This diagram shows how each class inherits from `Vehicle` or its subclasses. The `virtual` method `Accelerate` in `Vehicle` is overridden in the derived classes (`Land`, `Sea`, `Train`, and `Forklift`), and `Forklift` introduces an additional method `RaiseForkLift`. The fields in each class represent specific characteristics relevant to each type of vehicle.

---

## Questions to Answer in the README.md

#### 1. **What is the purpose of the `virtual` keyword in C# and how does it work in the context of inheritance?**
#### 2. **Can you explain the difference between `override` and `new` keywords when used in derived classes in C#?**
#### 3. **How does the `override` keyword in C# affect method resolution at runtime?**
#### 4. **In what scenario would you use the `new` keyword in C# to hide a member of the base class?**
#### 5. **What happens if a derived class in C# overrides a `virtual` method from the base class without using the `override` keyword?**    
#### 6. **Can a `virtual` method in a base class in C# be overridden in multiple levels of derived classes? How does this affect the method behavior?**

---

## Rubric

## Rubric

| Name                  | Description                                                             | Points |
|-----------------------|-------------------------------------------------------------------------|--------|
| Project Structure     | The project is structured correctly with appropriate classes and files.  | 10     |
| Name Comment          | The author's name is included at the top of the project.                | 5      |
| Compilation           | The code compiles without errors or warnings.                            | 10     |
| GitHub Repository     | The project is hosted on GitHub, and the repository link is provided.   | 5      |
| README Content        | The README.md file contains well-written answers to all 6 questions.    | 30     |
| Class Implementation  | All classes (`Vehicle`, `Land`, `Sea`, `Train`, `Forklift`) are correctly implemented with fields and methods as specified. | 20 |
| Method Overrides      | Methods in derived classes correctly override the base class methods.  | 10     |
| Method Functionality  | Methods provide the expected functionality, and outputs are correct.    | 10     |
| Code Testing          | Instances of each class are created, and `Accelerate` methods are called for testing. | 5 |
| Extra Credit (Optional) | Account, BankAccount, and CheckingAccount classes are implemented and tested. | 10 |
| Total Points          |                                                                       | 100    |
