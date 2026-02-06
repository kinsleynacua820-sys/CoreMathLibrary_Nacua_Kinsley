# CoreMathLibrary_Nacua_Kinsley

Overview:
The Core Math Library is a modular Java library designed using Object-Oriented Programming (OOP) principles. It organizes mathematical computations into reusable classes grouped by functionality: arithmetic operations, geometry calculations, and number analysis. The design focuses on inheritance, encapsulation, and clear class responsibilities to ensure the system is maintainable and extensible.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Class Responsibilities:
Each class in the library has a single, clear purpose:

MathematicalOperationParent (Parent Class):
* Stores shared data for arithmetic computations (first number and second number).
* Provides getter and setter methods.
* Declares a general `calculate()` method to be overridden.

Arithmetic Classes:
* Addition: Computes the sum of two numbers.
* Subtraction: Computes the difference between two numbers.
* Multiplication: Computes the product of two numbers.
* Division: Computes the quotient and handles division-by-zero cases.

ShapeParent (Parent Class):
* Defines behavior common to all geometric shapes.
* Declares methods for calculating area and perimeter.

Geometry Classes:
* Circle: Computes area and circumference using a radius.
* Rectangle: Computes area and perimeter using length and width.

NumberOperationParent (Parent Class):
* Stores a single number for analysis.
* Provides controlled access through getter and setter methods.

Number Analysis Classes:
* PrimeCheck: Determines whether a number is prime.
* Factorial: Computes the factorial of a number.
* EvenOdd: Determines whether a number is even or odd.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Inheritance Structure:
The system is organized into multiple inheritance hierarchies based on shared responsibilities.

Arithmetic operations inherit from `MathematicalOperationParent` because they all require two input values and a calculation behavior. Geometry classes inherit from `ShapeParent` since all shapes must compute area and perimeter. Number analysis classes inherit from `NumberOperationParent` because they operate on a single numeric value.

This structure reduces duplication, keeps related logic grouped together, and allows new operations to be added easily by extending existing parent classes.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Encapsulation Implementation:

Encapsulation is applied by declaring all class attributes as private and providing public getter and setter methods to control access. This prevents direct modification of internal data and ensures that validation rules can be enforced within each class.

Like for example the shape dimensions like radius, length, and width cannot be accessed directly. They must be set using setter methods, which can check for invalid values like negative inputs. Similarly, arithmetic and number analysis classes protect their input values from external manipulation.

By restricting access to internal data, the library maintains data integrity, prevents unintended changes, and ensures that all computations remain accurate and reliable.
