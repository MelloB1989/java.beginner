### 1. Reverse a String

```java
public String reverseString(String str) {
    return new StringBuilder(str).reverse().toString();
}
```

**Explanation**: Using the `StringBuilder` class to reverse a string easily.

---

### 2. Check for Palindrome

```java
public boolean isPalindrome(String str) {
    String reversed = new StringBuilder(str).reverse().toString();
    return str.equals(reversed);
}
```

**Explanation**: A palindrome is a word, phrase, number, or other sequences of characters that reads the same forward and backward (ignoring spaces, punctuation, and capitalization).

---

### 3. Count Vowels in a String

```java
public int countVowels(String str) {
    int count = 0;
    String vowels = "AEIOUaeiou";
    for(char c : str.toCharArray()) {
        if(vowels.indexOf(c) != -1) {
            count++;
        }
    }
    return count;
}
```

**Explanation**: Iterates over the string and checks if each character is a vowel.

---

### 4. Armstrong Number

An Armstrong number of three digits is an integer such that the sum of the cubes of its digits is equal to the number itself.

```java
public boolean isArmstrong(int num) {
    int original = num, result = 0;
    while (num != 0) {
        int remainder = num % 10;
        result += remainder * remainder * remainder;
        num /= 10;
    }
    return original == result;
}
```

---

### 5. Check Prime Number

```java
public boolean isPrime(int num) {
    if (num <= 1) {
        return false;
    }
    for (int i = 2; i <= Math.sqrt(num); i++) {
        if (num % i == 0) {
            return false;
        }
    }
    return true;
}
```

**Explanation**: A prime number is a number greater than 1 and can't be formed by multiplying two smaller natural numbers.

---

### 6. Fibonacci Series

```java
public void fibonacci(int count) {
    int a = 0, b = 1;
    System.out.print(a + " " + b);
    for (int i = 2; i < count; i++) {
        int next = a + b;
        System.out.print(" " + next);
        a = b;
        b = next;
    }
}
```

**Explanation**: The Fibonacci sequence is a series where the next number is the sum of the previous two numbers.

---

### 7. Duplicate Characters in a String

```java
public void findDuplicates(String str) {
    int[] counts = new int[256];
    for (char c : str.toCharArray()) {
        counts[c]++;
    }
    for (int i = 0; i < 256; i++) {
        if (counts[i] > 1) {
            System.out.printf("%c appears %d times%n", (char) i, counts[i]);
        }
    }
}
```

**Explanation**: Finds and prints characters that appear more than once in a string.

---

### 8. Factorial of a Number using Recursion

```java
public int factorial(int n) {
    if (n <= 1) {
        return 1;
    }
    return n * factorial(n - 1);
}
```

**Explanation**: The factorial of a non-negative integer n is the product of all positive integers less than or equal to n.

---

### 9. Removing White Spaces from a String

```java
public String removeWhiteSpaces(String str) {
    return str.replaceAll("\\s+", "");
}
```

**Explanation**: Uses regular expressions to replace all sequences of whitespace characters with an empty string.

---

### 10. Count Occurrence of a Character

```java
public int countOccurrences(String str, char c) {
    int count = 0;
    for (char ch : str.toCharArray()) {
        if (ch == c) {
            count++;
        }
    }
    return count;
}
```

**Explanation**: Iterates over the string and counts the occurrences of the specified character.
