---

## Java Quick Review: Datatypes, Variables, Expressions, and Operators

### 1. Datatypes

Java is a statically-typed language, which means you must declare the type of a variable before using it. There are two categories of data types in Java:

#### 1.1. Primitive Datatypes

These are built-in data types:

- **Numeric Types**
  - `byte`: 8-bit integer. Range: -128 to 127.
  - `short`: 16-bit integer. Range: -32,768 to 32,767.
  - `int`: 32-bit integer. Range: ~-2 billion to ~2 billion.
  - `long`: 64-bit integer. 
  - `float`: 32-bit floating point.
  - `double`: 64-bit floating point.

- **Character Type**
  - `char`: Represents a single 16-bit Unicode character.

- **Boolean Type**
  - `boolean`: Represents a true or false value.

#### 1.2. Reference Datatypes

- These are references to objects. Examples include arrays and objects of any class. Unlike primitive types, reference types are initialized to `null` by default.

### 2. Variables

Variables are used to store data for processing. A variable has a datatype and a name (identifier).

```java
int age = 25;      // 'int' is the datatype, 'age' is the variable name, and '25' is the value.
char letter = 'A'; 
boolean isActive = true;
```

### 3. Expressions

An expression is a combination of variables, values, and operators that can be evaluated.

```java
int result = 10 + 20; // '10 + 20' is an expression.
```

### 4. Operators

Operators are used to perform operations on variables and values. Here are the main types:

#### 4.1. Arithmetic Operators

- `+`: Addition
- `-`: Subtraction
- `*`: Multiplication
- `/`: Division
- `%`: Modulus (remainder)

#### 4.2. Relational Operators

- `==`: Equal to
- `!=`: Not equal to
- `>`: Greater than
- `<`: Less than
- `>=`: Greater than or equal to
- `<=`: Less than or equal to

#### 4.3. Logical Operators

- `&&`: Logical AND
- `||`: Logical OR
- `!`: Logical NOT

#### 4.4. Assignment Operators

- `=`: Assign
- `+=`: Add and assign
- `-=`: Subtract and assign
- `*=`: Multiply and assign
- `/=`: Divide and assign
- `%=`: Modulus and assign

#### 4.5. Unary Operators

- `+`: Unary plus
- `-`: Unary minus (negation)
- `++`: Increment
- `--`: Decrement

---
