# Swift Classes Interview Questions (Beginner to Advanced)

## Beginner Level

1. **What is a class in Swift?**  
   *Answer*
   - In Swift, A **class** is a blueprint or template used to create objects, which are instances of that class. It allows for defining **properties** (data) and **methods** (functions) that can perform actions using those properties. Classes are reference types, meaning objects created from the same class share the same memory reference.
   ```swift
    class Person {
      var name: String
      var age: Int
    
        init(name: String, age: Int) {
            self.name = name
            self.age = age
        }
    
        func greet() {
            print("Hello, my name is \(name).")
        }
    }
2. **How does a class differ from a structure?**  
   *Answer*
    - **Class** is a ***reference type***, while **Struct** is a ***value type***.
    - When you assign or pass a class instance, you are passing a reference to the same memory, but with a struct, you are passing a copy.
    - Classes support inheritance, while structs do not.
    - Classes can be deinitialized, while structs cannot.
    ```swift
    struct Car {
        var model: String
    }
        
    class Vehicle {
        var model: String
    
        init(model: String) {
            self.model = model
        }
    }

    var car1 = Car(model: "Sedan")
    var car2 = car1
    car2.model = "SUV"
    print(car1.model)  // Output: Sedan

    var vehicle1 = Vehicle(model: "Sedan")
    var vehicle2 = vehicle1
    vehicle2.model = "SUV"
    print(vehicle1.model)  // Output: SUV

 In the above example, the **struct** copy doesn’t affect the original, but the **class** reference does.

3. **How do you create an instance of a class in Swift?**  
   *Answer*
    To create an instance of a class, you initialize the class using the init method.
    ```swift
    let person = Person(name: "Priyank", age: 30)
    person.greet() // Output: Hello, my name is Priyank.

4. **What are properties in a class?**  
   *Answer*
   Properties in a class are variables or constants that hold data for the class. There are two types:
   - **Stored Properties:** Store actual values.
   - **Computed Properties:** Calculate values dynamically.
   ```swift
    class Circle {
        var radius: Double
        var area: Double {
            return 3.14 * radius * radius
        }
    
        init(radius: Double) {
            self.radius = radius
        }
    }

In above example, radius is a *stored property* and area is a *computed property*.

5. **How do you declare methods inside a class?**  
   *Answer*
   Methods in a class are declared like functions inside the class scope. They can access the class's properties and other methods.
    ```swift
    class Animal {
        var name: String
    
        init(name: String) {
            self.name = name
        }
    
        func sound() {
            print("\(name) makes a sound.")
        }
    }

6. **What is a designated initializer?**  
   *Answer*
   A **designated initializer** is the primary initializer for a class that fully initializes all properties and calls the superclass's initializer (if applicable). It’s the main entry point for creating instances of the class.
    ```swift
    class Rectangle {
        var width: Double
        var height: Double
    
        // Designated Initializer
        init(width: Double, height: Double) {
            self.width = width
            self.height = height
        }
    }

7. **What is the difference between a class and an object?**  
   *Answer*
    -  A **class** is a blueprint that defines the properties and methods.
    -  An **object (or instance)** is an actual realization of the class.

    You can think of a **class** as the definition of a house, and an **object** as the actual house built from that definition.
    ```swift
    class Dog {
        var breed: String
    
        init(breed: String) {
            self.breed = breed
        }
    }

    let dog = Dog(breed: "Labrador")
    
* In above example, *Dog* is the **class**, and *dog* is the **object** created from that class.

8. **How do you define static properties in a class?**  
   *Answer*
   A **static property** in a class is shared by all instances of the class. It's defined using the static keyword and is associated with the class itself rather than any instance.
   
    ```swift
    class Planet {
        static var planetCount = 0
        var name: String
    
        init(name: String) {
            self.name = name
            Planet.planetCount += 1
        }
    }

    let earth = Planet(name: "Earth")
    let mars = Planet(name: "Mars")

    print(Planet.planetCount) // Output: 2

9. **What is inheritance in Swift?**  
   *Answer*
   **Inheritance** allows one class to inherit properties, methods, and other characteristics from another class. In Swift, this is done using a colon (`:`) after the class name.

   ```swift
   class Vehicle {
        var speed: Int = 0
        func drive() {
            print("Driving at \(speed) mph")
        }
    }

    class Car: Vehicle {
        var model: String
    
        init(model: String) {
            self.model = model
            super.init()  // Calls the superclass initializer
        }
    
        override func drive() {
            print("Car \(model) driving at \(speed) mph")
        }
    }

    let myCar = Car(model: "Tesla")
    myCar.speed = 60
    myCar.drive()  // Output: Car Tesla driving at 60 mph

- In this example, *Car* **inherits** from *Vehicle*.

10. **Can a class have default property values?**  
    *Answer*
    Yes, a class can have default property values. This means that if a property is not explicitly initialized, it will take the default value.

    ```swift
    class User {
        var name: String = "Guest"
        var age: Int = 18
    }

    let newUser = User()
    print(newUser.name)  // Output: Guest
    
---

## Intermediate Level

1. **What is method overriding? Provide an example.**  
    *Answer coming soon...*

2. **Explain how subclassing works in Swift.**  
    *Answer coming soon...*

3. **What is a convenience initializer?**  
    *Answer coming soon...*

4. **What is the role of `super.init()` in subclassing?**  
    *Answer coming soon...*

5. **How does Swift handle access control with classes (e.g., public, private)?**  
    *Answer coming soon...*

6. **What are computed properties in a class?**  
    *Answer coming soon...*

7. **Explain how optional chaining works with class properties.**  
    *Answer coming soon...*

8. **What are class methods in Swift?**  
    *Answer coming soon...*

9. **Explain the concept of class inheritance.**  
    *Answer coming soon...*

10. **What are deinitializers, and when are they called?**  
    *Answer coming soon...*

---

## Advanced Level

1. **What is the difference between a reference type and a value type?**  
    *Answer coming soon...*

2. **How do reference counting and memory management work with classes?**  
    *Answer coming soon...*

3. **How do you avoid retain cycles in classes?**  
    *Answer coming soon...*

4. **Explain method dispatch in Swift.**  
    *Answer coming soon...*

5. **Can a class conform to a protocol? Provide an example.**  
    *Answer coming soon...*

6. **What is polymorphism, and how does it work with classes?**  
    *Answer coming soon...*

7. **How does the `required` keyword affect class initializers?**  
    *Answer coming soon...*

8. **How do you create abstract classes in Swift?**  
    *Answer coming soon...*

9. **Can you explain how class clusters are used in Swift?**  
    *Answer coming soon...*

10. **How does Swift handle dynamic method dispatching?**  
    *Answer coming soon...*
