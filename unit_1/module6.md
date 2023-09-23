# JAVA: Nested Classes and Strings

## 1. Nested and Inner Classes

In Java, a class can be declared within another class. Such a class is known as a nested class.

### **Types of Nested Classes:**

1. **Static Nested Class**: A static class inside another class.
   ```java
   class OuterClass {
       static class NestedClass {
       }
   }
   ```

2. **Inner Class (or Non-static Nested Class)**: A non-static class inside another class.
   ```java
   class OuterClass {
       class InnerClass {
       }
   }
   ```

3. **Local Inner Class**: Defined within a method of the outer class.
   
4. **Anonymous Inner Class**: An inner class without a name, usually used for overriding methods.

### **Usage:**

- **Logical Grouping**: If a class is useful to only one other class, then it's logical to nest it.
  
- **Increased Encapsulation**: Nested classes can access private members of the outer class, which can help in increasing encapsulation.
  
- **Cleaner Code**: Helps in writing more readable and maintainable code.

---

## 2. Strings

In Java, strings are objects that represent sequences of characters.

### **String Creation:**

1. **Using String literal**:
   ```java
   String str1 = "Hello";
   ```

2. **Using new keyword**:
   ```java
   String str2 = new String("Hello");
   ```

### **Immutability**: 

Strings in Java are immutable, which means once a String object is created, it cannot be changed. If you perform any operation on a string, a new string object is created.

---

## 3. String Constructors

There are multiple constructors available in the String class. Here are a few:

1. **String()**: Initializes a newly created String object so that it represents an empty character sequence.
   
2. **String(String original)**: Initializes a newly created String object so that it represents the same sequence of characters as the argument.
   
3. **String(char[] value)**: Allocates a new String so that it represents the character sequence currently contained in the character array argument.

---

## 4. String Functions

The String class in Java has a plethora of functions. Here are some commonly used ones:

1. **length()**: Returns the length of the string.
   
2. **charAt(int index)**: Returns the character at the specified index.
   
3. **substring(int beginIndex, int endIndex)**: Returns a substring.
   
4. **equals(Object obj)**: Compares the content of the strings.
   
5. **equalsIgnoreCase(String anotherString)**: Compares the content of strings, ignoring case differences.
   
6. **contains(CharSequence sequence)**: Checks if the string contains the specified sequence of characters.
   
7. **replace(char oldChar, char newChar)**: Replaces all occurrences of the specified char.
   
8. **trim()**: Removes whitespace from both ends of a string.

---

## Summary:

- **Nested and Inner Classes**: Classes defined within another class, aiding in logical grouping and encapsulation.
  
- **Strings**: Immutable objects in Java that represent sequences of characters. Can be created using literals or the `new` keyword.
  
- **String Constructors**: Different ways to create string objects, including using existing strings, character arrays, and others.
  
- **String Functions**: The String class provides numerous functions for string manipulation, such as finding length, comparing strings, extracting substrings, and more.
