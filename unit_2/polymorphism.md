## 1. Polymorphism

Polymorphism is derived from two Greek words: *poly* (many) and *morphs* (forms). It allows you to use an object of a subclass in place of an object of its superclass and to write methods that work on objects of different classes if they are related by inheritance.

There are two types of polymorphism in Java:
1. **Compile-time Polymorphism (Method Overloading)**
2. **Run-time Polymorphism (Method Overriding)**

Here, we'll focus more on the run-time aspect since method overloading was covered earlier.

---

## 2. Method Overriding (Run-time Polymorphism)

When a subclass provides a specific implementation for a method that is already defined in its superclass, it's known as method overriding. This is done to either provide a specific implementation or to extend the existing one.

**Rules for Method Overriding**:
- The method must have the same name as in the parent class.
- The method must have the same parameter as in the parent class.
- There must be an IS-A relationship (inheritance).

**Example**:
```java
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks");
    }
}
```

Usage:
```java
Animal obj = new Dog();
obj.sound();  // Outputs: Dog barks
```

---

## 3. Abstract Classes

An abstract class is a class that cannot be instantiated. It can only be subclassed. It often contains abstract methods that must be implemented in any derived classes.

**Characteristics**:
- Cannot be instantiated.
- Can contain both abstract and non-abstract methods.
- Can have variables, constructors, and static methods.

**Example**:
```java
abstract class Shape {
    int width;
    abstract void area();
}
```

---

## 4. Object Class

The Object class in Java is the root class of the Java class hierarchy. Every class in Java directly or indirectly inherits from the Object class. It provides a handful of essential methods, such as:

- **hashCode()**: Returns a hash code for the object.
- **equals(Object obj)**: Compares the instance with the object.
- **toString()**: Returns a string representation of the object.
- **clone()**: Creates a new instance that's a copy of the object.

---

## Summary:

- **Polymorphism**: Allows objects of different classes to be treated as objects of a common superclass. It enhances the flexibility and reusability of code.
  
- **Method Overriding**: Helps achieve runtime polymorphism. A subclass provides its own implementation for a method already defined in the superclass.
  
- **Abstract Classes**: Cannot be instantiated and often act as a base class, providing a template for other classes.
  
- **Object Class**: The root of the Java class hierarchy. Provides some essential methods that are available to every object in Java.
