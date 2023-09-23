## Java Quick Review: Arrays, 2D Arrays, Control Statements, and Type Casting

### 1. Arrays

Arrays are used to store multiple values in a single variable.

#### 1.1. Declaration & Initialization

```java
int[] numbers = new int[5];       // Declares an array of size 5. All values are initialized to 0.
int[] predefinedNumbers = {1, 2, 3, 4, 5};   // Declares and initializes the array.
```

#### 1.2. Accessing Array Elements

```java
int firstNumber = numbers[0];  // Accessing the first element.
numbers[4] = 10;               // Setting the value of the last element.
```

#### 1.3. Array Length

```java
int arraySize = numbers.length;  // Gives the size of the array.
```

### 2. 2D Arrays (Matrices or Tables)

2D arrays are essentially "arrays of arrays".

#### 2.1. Declaration & Initialization

```java
int[][] matrix = new int[3][3];  // 3x3 matrix.
int[][] predefinedMatrix = { {1, 2, 3}, {4, 5, 6}, {7, 8, 9} };
```

#### 2.2. Accessing 2D Array Elements

```java
int element = matrix[1][2];    // Accesses the element in the second row, third column.
matrix[0][0] = 10;             // Sets the value of the first element of the first row.
```

### 3. Control Statements

Control statements allow you to control the flow of program's execution based on conditions or loops.

#### 3.1. Conditional Statements

- **if statement**:

```java
if (condition) {
    // Executes when condition is true.
}
```

- **if-else statement**:

```java
if (condition) {
    // Executes when condition is true.
} else {
    // Executes when condition is false.
}
```

- **switch statement**:

```java
switch (variable) {
    case value1:
        // Code to execute for value1.
        break;
    case value2:
        // Code to execute for value2.
        break;
    default:
        // Code to execute if none of the cases match.
}
```

#### 3.2. Looping Statements

- **for loop**:

```java
for (initialization; condition; update) {
    // Code to be repeated.
}
```

- **while loop**:

```java
while (condition) {
    // Code to be repeated.
}
```

- **do-while loop**:

```java
do {
    // Code to be repeated.
} while (condition);
```

- **enhanced for loop** (for arrays and collections):

```java
for (datatype item : iterable) {
    // Use item.
}
```

### 4. Type Casting

Type casting is converting variables from one type to another.

#### 4.1. Widening Casting (automatically done)

```java
int myInt = 9;
double myDouble = myInt;  // Int to double.
```

#### 4.2. Narrowing Casting (must be done manually)

```java
double myDouble = 9.78;
int myInt = (int) myDouble;  // Double to int. Decimal part is truncated.
```
