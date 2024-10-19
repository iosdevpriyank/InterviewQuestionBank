# 📚 InterviewQuestionBank

Welcome to the **InterviewQuestionBank**, a curated resource for mastering technical interviews. This repository provides comprehensive questions and detailed answers across various Swift, iOS, and software engineering topics.

## 📁 Topics

1. [Classes](./topics/Classes.md)
2. [Structures](./topics/Structures.md)
3. [Actors](./topics/Actors.md)
4. [Properties & Initializers](./topics/Properties_Initializers.md)
5. [Enumerations](./topics/Enumerations.md)
6. [Functions, Methods & Closures](./topics/Functions_Methods_Closures.md)
7. [Protocol & Delegation](./topics/Protocol_Delegation.md)
8. [UIViewController Lifecycle](./topics/UIViewController_Lifecycle.md)
9. [UIKit Framework](./topics/UIKit_Framework.md)
10. [SwiftUI Framework](./topics/SwiftUI_Framework.md)
11. [Concurrency](./topics/Concurrency.md)
12. [Generics & Error Handling](./topics/Generics_ErrorHandling.md)
13. [Networking](./topics/Networking.md)
14. [Combine Framework](./topics/Combine_Framework.md)
15. [Memory Management](./topics/Memory_Management.md)
16. [App Performance](./topics/App_Performance.md)
17. [App Security](./topics/App_Security.md)
18. [SOLID Principles](./topics/SOLID_Principles.md)
19. [Bluetooth, WebSocket, IoT](./topics/Bluetooth_WebSocket_IoT.md)
20. [Miscellaneous Swift Questions](./topics/Miscellaneous.md)

---

## 📝 How to Use:

- Click on any topic above to access its dedicated question bank.
- Each file contains multiple **questions** along with **detailed answers** and code examples.
- Feel free to contribute or open an issue if you'd like to see additional topics covered!

---

## 💡 Contributions

We welcome contributions from the community. If you have new interview questions or improvements to existing answers, feel free to submit a pull request or open an issue.

1. Fork this repository
2. Add your changes or new questions under the respective topic file
3. Submit a pull request

---

### Example: Question Format

Here’s how each question will be formatted inside each topic file:

---

### Question 1: What is a Class in Swift?

**Answer:**
A class in Swift is a blueprint for creating objects. It supports inheritance, meaning you can create subclasses that inherit properties and methods from the parent class.

```swift
class Animal {
    var name: String
    init(name: String) {
        self.name = name
    }
    func speak() {
        print("\(name) makes a sound")
    }
}
