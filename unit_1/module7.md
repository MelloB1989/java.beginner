# JAVA: Recursion and parameter passing

## 1. Recursion

Recursion is a programming concept where a function calls itself to solve a bigger problem by breaking it down into smaller, more manageable problems.

### **Characteristics**:

1. **Base Case**: Every recursive function should have a condition that stops the recursion, known as the base case.

2. **Recursive Call**: A function making a call to itself.

### **Example**:

A classic example is the calculation of the factorial of a number:

```java
public int factorial(int n) {
    if (n <= 1) { // Base case
        return 1;
    }
    return n * factorial(n-1); // Recursive call
}
```

### **Note**:

- Recursion can be elegant but may lead to a stack overflow error if the recursion is too deep.

---

## 2. Call by Value vs Call by Reference

Java uses both "call by value" and what's colloquially known as "call by reference". However, it's essential to clarify that Java strictly uses "call by value", but the values being passed can be references.

### **Call by Value**:

For **primitive data types**, Java uses call by value. This means that when you pass a primitive data type to a method, a copy of the value is passed, and the original value remains unchanged.

**Example**:
```java
void modify(int value) {
    value = value + 100;
}
int num = 50;
modify(num);
System.out.println(num);  // This will print 50, not 150.
```

### **Call by Reference**:

For **objects**, Java passes the reference by value. This means that the method receives a reference to the object, and changes made to the object within the method reflect outside of it.

**Example**:
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

### **Key Distinction**:

- With **primitives**, the method gets a copy of the actual value.
  
- With **objects**, the method gets a copy of the reference to the object.

---

## Summary:

- **Recursion**: A technique where a function calls itself. It breaks down problems into smaller chunks but must have a base case to prevent infinite loops.
  
- **Call by Value**: For primitive types, the method gets a copy of the actual value, ensuring the original variable remains unaffected.
  
- **Call by Reference (Reference by Value)**: For objects, the method gets a copy of the reference to the object. This allows the method to modify the object being referred to.
