## Java Concepts: Overloading, Call by Value, and Call by Reference

### 1. Method Overloading

Method overloading allows a class to have multiple methods with the same name, but with different parameters.

#### Benefits:

- Increases the readability of the program.
- Allows defining methods that perform similar tasks using a single name.

#### Rules:

- Methods must have a different number or type of parameters.
- Change in return type alone is insufficient.

#### Example:

```java
class MathOperation {
    int sum(int a, int b) {
        return a + b;
    }
    
    double sum(double a, double b) {
        return a + b;
    }
    
    int sum(int a, int b, int c) {
        return a + b + c;
    }
}
```

### 2. Constructor Overloading

Like methods, constructors can also be overloaded. This allows an object to be initialized in different ways.

#### Example:

```java
class Rectangle {
    int length;
    int breadth;
    
    // Constructor to initialize both dimensions
    Rectangle(int l, int b) {
        length = l;
        breadth = b;
    }

    // Constructor to initialize a square
    Rectangle(int side) {
        length = breadth = side;
    }
}
```

### 3. Call by Value

Java uses **call by value** for primitive data types. This means that when you pass a primitive data type to a method, a copy of the value is passed, and the original value remains unchanged.

#### Example:

```java
void modify(int value) {
    value = value + 100;
}

int num = 50;
modify(num);
System.out.println(num);  // This will print 50, not 150.
```

### 4. Call by Reference

Java uses **call by reference** for objects. When you pass an object to a method, a reference to the object is passed. Any changes made to the object within the method are reflected outside of it.

#### Note: 
Strictly speaking, Java still uses "call by value" for objects. But the "value" being passed is the reference to the object, not the actual object. Therefore, it's commonly referred to as "call by reference" in a colloquial sense.

#### Example:

```java
class Number {
    int val = 50;
}

void modify(Number numberObj) {
    numberObj.val = numberObj.val + 100;
}

Number myNum = new Number();
modify(myNum);
System.out.println(myNum.val);  // This will print 150.
```

---

## Key Takeaways:

- **Overloading**: Allows a class to have multiple methods or constructors with the same name but different parameters.
  
- **Call by Value**: For primitives, the method receives a copy of the value. Original remains unchanged.
  
- **Call by Reference**: For objects, the method receives a reference to the object. Changes inside the method affect the original object.
