## Java Concepts: `this` Keyword, `static` Keyword, and Garbage Collection

### 1. `this` Keyword

The `this` keyword refers to the current instance of the class. It can be used to:

1. **Refer to instance variables**: Distinguish between class attributes and method parameters when they have the same names.
2. **Invoke current class methods**: Useful in method chaining.
3. **Return the current class instance**: Especially helpful in method chaining.
4. **Invoke current class constructors**: Use `this()` to call a constructor from another constructor.

#### Example:

```java
class Book {
    String title;

    Book(String title) {
        this.title = title;  // Differentiates between class attribute and constructor parameter
    }
    
    void display() {
        System.out.println("Title: " + this.title);
    }
}
```

### 2. `static` Keyword

The `static` keyword denotes that a member belongs to the class rather than any specific instance. It can be applied to:

1. **Variables**: These are shared among all instances of a class.
2. **Methods**: These can be called on the class itself rather than on instances.
3. **Blocks**: These are used for static initializations.
4. **Inner Classes**: Denotes the class is a static member of the outer class.

#### Example:

```java
class Counter {
    static int count = 0;  // Static variable
    
    Counter() {
        count++;
    }
    
    static void displayCount() {  // Static method
        System.out.println("Count: " + count);
    }
}
```

### 3. Garbage Collection

In Java, memory management is mainly done through automatic garbage collection.

1. **What it is**: The process by which Java automatically deletes objects that are no longer referenced to free up memory.
2. **How it works**: The Java Virtual Machine (JVM) has a garbage collector that periodically checks for unreferenced objects and deletes them.
3. **`finalize()` method**: It's called by the garbage collector on an object when garbage collection determines that there are no more references to the object.
4. **Explicitly Requesting Garbage Collection**: Though not recommended (since the JVM handles this), you can request the garbage collector to run using `System.gc()`.

#### Key Points:

- Java garbage collection makes coding in Java easier since developers don't have to manage memory manually.
- However, it's essential to be aware of it to write efficient programs and avoid memory leaks.

---

## Summary:

- **`this` Keyword**: Refers to the current instance of the class.
- **`static` Keyword**: Denotes class-level members. They're shared across instances and can be accessed without creating an object of the class.
- **Garbage Collection**: An automated system in Java that manages memory by reclaiming the runtime unused memory automatically.
