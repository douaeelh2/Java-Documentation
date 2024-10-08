# Java Fundamentals Documentation

<div>
  <img src="https://github.com/douaeelh2/Java-Documentation/assets/127549220/cec272f8-1c6e-4fcd-b4a8-cbc20b73724d" alt="Java Image"  style="width: 90%">
</div>

This documentation aims to provide an overview of fundamental Java 8 , 11 , 17 and 21 Concepts necessary for working with Spring Framework.

# Table of Contents

- [What is JDK, JRE and JVM in Java](#what-is-jdk-jre-and-jvm-in-java)
- [How to Execute a Java Program](#how-to-execute-a-java-program)

- [Java Basics](#java-basics)
  - [Variables](#variables)
  - [Data Types](#data-types)
  - [Operators](#operators)
  - [Control Flow Statements](#control-flow-statements)
    - [If-Else](#if-else)
    - [Switch](#switch)
  - [Loops](#loops)
    - [For Loop](#for-loop)
    - [While Loop](#while-loop)
    - [Do-While Loop](#do-while-loop)
  - [Arrays](#arrays)
  - [String Manipulation](#string-manipulation)
  - [Exception Handling](#exception-handling)
  
- [Java 8 Basics](#java-8-basics)
  - [Lambda Expressions](#java-lambda-expressions)
  - [Functional Interfaces](#java-functional-interfaces)
  - [Static and Default Methods in Interface](#java-static-and-default-methods-in-interface)
  - [Collection Interfaces](#collection-interfaces)
  - [Stream API](#java-stream-api)
  - [Optional Class](#java-optional-class)
  - [StringJoiner Class](#java-stringjoiner-class)

- [Java 11 Basics](#java-11-basics)
  - [New String Methods](#java-new-string-methods)
  - [HttpClient API](#java-httpclient-api)

- [Java OOP (Object-Oriented Programming)](#java-oop-object-oriented-programming)
  - [Encapsulation](#encapsulation)
  - [Inheritance](#inheritance)
  - [Abstraction](#abstraction)
  - [Polymorphism](#polymorphism)
  - [Aggregation & Composition](#aggregation-&-composition)
  - [Interface & Abstract Class](#interface-&-abstract-class)
  - [Static](#static)
  - [Final](#final)



# What is JDK, JRE and JVM in Java
 ## 1. JDK (Java Development Kit)
   - The `JDK (Java Development Kit)` is a superset of the JRE and contains everything that is in the JRE, plus tools such as the compiler, debugger, JavaDoc, keytool etc necessary for developing and running Java programs or applications.
     
     
     ![Java JDK JRE and JVM](https://github.com/douaeelh2/Java-Documentation/assets/127549220/ab43eb26-79a7-4936-8ace-10da5a248a51)

 ## 2. JVM (Java Virtual Machine)
   - The `JVM (Java Virtual Machine)` is a very important component of Java programming language. When you run the Java program, the Java compiler first compiles your Java code to bytecode. Then, the JVM translates bytecode into native machine code (set of instructions that a computer's CPU executes directly).
   - `JVM` is called virtual because it provides an interface that does not depend on the underlying operating system and machine hardware.
  
     ![JVM](https://github.com/douaeelh2/Java-Documentation/assets/127549220/2b0cfefd-eae7-405d-8d67-be6492089df4)
     

 ## 3. JRE (Java Runtime Environment)
   - The `Java Runtime Environment (JRE)` provides the libraries, the Java Virtual Machine, and other components to run applets and applications written in the Java programming language.
JRE doesn’t contain any development tools such as Java compiler, debugger, JShell, etc.
   - If you just want to execute a java program, you can install only JRE. You don’t need JDK because there is no development or compilation of java source code is required.

   ![JRE](https://github.com/douaeelh2/Java-Documentation/assets/127549220/30dc98dd-e601-47c5-b516-1fa1cc03797e)
   

# How to Execute a Java Program
 ### 1. Writing the Source Code 
   - Begin by writing your Java program using a text editor or an Integrated Development Environment (IDE) such as Eclipse, Netbeans, or IntelliJ IDEA. Save the Java source code in files with the .java extension.

 ## 2. Compilation:
   - Compile your Java source code into bytecode using a Java compiler included in the `Java Development Kit (JDK)`. You can compile your code using the `javac` command-line tool or built-in features of an IDE. Compilation converts your Java source code into `.class ` files containing Java bytecode.

## 3. Runtime Environment (JRE)
   - To execute the Java bytecode, install the `Java Runtime Environment (JRE)`, which includes the `Java Virtual Machine (JVM)` and standard Java class libraries. The JRE provides an environment for executing Java bytecode.

## 4. Running the Program
   - Once the JRE is installed, run your Java program using the `java` command followed by the name of the class containing the `main()` method in your terminal or command prompt.


# Java Basics
## Variables

In Java, **variables** are containers that store data values. Each variable must be declared with a **data type**, which defines the type of value the variable can store.

A variable in Java has three key components:

- **Data Type**: Specifies the type of data the variable will hold (e.g., `int`, `String`).
- **Variable Name**: The name of the variable (follows naming conventions).
- **Value**: The data or value assigned to the variable.

### Types of Variables

1. **Local Variables**: Declared inside a method, constructor, or block and are only accessible within that scope.
2. **Instance Variables**: Declared in a class, but outside a method, constructor, or block. They are non-static and each object has its own copy.
3. **Static Variables**: Declared using the `static` keyword, and they are shared among all objects of the class.

##### Example:

```java
    public class Example {
        // Instance variable
        int instanceVar = 10;
    
        // Static variable
        static int staticVar = 20;
    
        public void method() {
            // Local variable
            int localVar = 30;
            System.out.println(localVar);
        }
    }
```

 ## Data Types
Java has two main types of data types:

- **Primitive Data Types:** Predefined by the language and store simple values.
- **Reference Data Types:** Created using classes and store references (addresses) to objects.
  
### 1. Primitive Data Types

Java provides 8 primitive data types:


| Data Type | Size     | Default Value | Description                          |
|-----------|----------|---------------|--------------------------------------|
| `byte`    | 1 byte   | 0             | Stores small integers (-128 to 127). |
| `short`   | 2 bytes  | 0             | Stores small integers (-32,768 to 32,767). |
| `int`     | 4 bytes  | 0             | Stores whole numbers (-2^31 to 2^31-1). |
| `long`    | 8 bytes  | 0L            | Stores large integers (-2^63 to 2^63-1). |
| `float`   | 4 bytes  | 0.0f          | Stores fractional numbers with up to 7 decimal digits. |
| `double`  | 8 bytes  | 0.0d          | Stores fractional numbers with up to 16 decimal digits. |
| `char`    | 2 bytes  | '\\u0000'     | Stores a single 16-bit Unicode character. |
| `boolean` | 1 bit    | `false`       | Stores a `true` or `false` value.   |



#### Example

```java
    public class DataTypesExample {
        public static void main(String[] args) {
            byte b = 100;
            short s = 1000;
            int i = 10000;
            long l = 100000L;
    
            float f = 10.5f;
            double d = 20.99;
    
            char c = 'A';
            boolean bool = true;
    
            System.out.println("Byte: " + b);
            System.out.println("Short: " + s);
            System.out.println("Int: " + i);
            System.out.println("Long: " + l);
            System.out.println("Float: " + f);
            System.out.println("Double: " + d);
            System.out.println("Char: " + c);
            System.out.println("Boolean: " + bool);
        }
    }
```
### 2. Reference Data Types
Reference data types include objects, arrays, and strings. These store memory addresses where data is located, rather than the actual value.

- **Class Objects:** Instances of user-defined classes.
- **Arrays:** Store multiple values of the same type.
- **Strings:** Special class in Java used to store sequences of characters.

Example:

```java
    public class ReferenceDataTypesExample {
      public static void main(String[] args) {
          // String (Reference Type)
          String str = "Hello, Java!";
          
          // Array (Reference Type)
          int[] numbers = {1, 2, 3, 4, 5};
  
          // Printing values
          System.out.println("String: " + str);
          System.out.println("First element in the array: " + numbers[0]);
      }
  }
```

### 3. Type Casting
When assigning values of one type to another, Java provides type casting.

- **Implicit Casting (Widening):** Automatically converts smaller data types to larger ones.
Example: `int` to `long`
- **Explicit Casting (Narrowing):** Manually converts larger data types to smaller ones.
Example: `double` to `int`

Example:

```java
    public class TypeCastingExample {
        public static void main(String[] args) {
            int intVal = 100;
            long longVal = intVal; // Implicit Casting (int to long)
    
            double doubleVal = 10.99;
            int intVal2 = (int) doubleVal; // Explicit Casting (double to int)
    
            System.out.println("Long value: " + longVal);
            System.out.println("Int value after casting: " + intVal2);
        }
    }
```


## Operators
In Java, operators are special symbols used to perform operations on variables and values. Java provides several types of operators to manipulate data, perform arithmetic calculations, compare values, and more.

### Types of Operators:

- **1. Arithmetic Operators**
- **2. Assignment Operators**
- **3. Relational (Comparison) Operators**
- **4. Logical Operators**
- **5. Bitwise Operators**
- **6. Unary Operators**
- **7. Ternary Operator**

### 1. Arithmetic Operators
Arithmetic operators are used to perform basic mathematical operations like addition, subtraction, multiplication, etc.

| Operator | Description       | Example    |
|----------|-------------------|------------|
| `+`      | Addition           | `a + b`    |
| `-`      | Subtraction        | `a - b`    |
| `*`      | Multiplication     | `a * b`    |
| `/`      | Division           | `a / b`    |
| `%`      | Modulus (remainder)| `a % b`    |

Example:

```java
    public class ArithmeticExample {
      public static void main(String[] args) {
          int a = 10, b = 5;
          System.out.println("Addition: " + (a + b));  // 15
          System.out.println("Subtraction: " + (a - b)); // 5
          System.out.println("Multiplication: " + (a * b)); // 50
          System.out.println("Division: " + (a / b)); // 2
          System.out.println("Modulus: " + (a % b)); // 0
      }
  }
```

### 2. Assignment Operators
Assignment operators are used to assign values to variables.

| Operator | Description            | Example    |
|----------|------------------------|------------|
| `=`      | Assign value            | `a = 10`   |
| `+=`     | Add and assign          | `a += 5`   |
| `-=`     | Subtract and assign     | `a -= 5`   |
| `*=`     | Multiply and assign     | `a *= 5`   |
| `/=`     | Divide and assign       | `a /= 5`   |
| `%=`     | Modulus and assign      | `a %= 5`   |

Example:

```java
     public class AssignmentExample {
      public static void main(String[] args) {
          int a = 10;
          a += 5; // a = a + 5
          System.out.println("a after += 5: " + a); // 15
          a *= 2; // a = a * 2
            System.out.println("a after *= 2: " + a); // 30
        }
    }
```

### 3. Relational (Comparison) Operators
Relational operators are used to compare two values. They return a boolean result (`true` or `false`).

| Operator | Description            | Example    |
|----------|------------------------|------------|
| `==`     | Equal to                | `a == b`   |
| `!=`     | Not equal to            | `a != b`   |
| `>`      | Greater than            | `a > b`    |
| `<`      | Less than               | `a < b`    |
| `>=`     | Greater than or equal to| `a >= b`   |
| `<=`     | Less than or equal to   | `a <= b`   |

Example:

```java
     public class ComparisonExample {
        public static void main(String[] args) {
            int a = 10, b = 5;
            System.out.println("a == b: " + (a == b)); // false
            System.out.println("a != b: " + (a != b)); // true
            System.out.println("a > b: " + (a > b)); // true
            System.out.println("a <= b: " + (a <= b)); // false
          }
      }
```

### 4. Logical Operators
Logical operators are used to combine two or more conditions. They work with boolean values (true or false).

| Operator | Description                | Example          |
|----------|----------------------------|------------------|
| `&&`     | Logical AND                 | `a && b`         |
| `||`     | Logical OR                  | `a || b`         |
| `!`      | Logical NOT                 | `!a`             |


```java
    public class LogicalExample {
        public static void main(String[] args) {
            boolean a = true, b = false;
            System.out.println("a && b: " + (a && b)); // false
            System.out.println("a || b: " + (a || b)); // true
            System.out.println("!a: " + (!a)); // false
        }
    }
```

### 5. Bitwise Operators
Bitwise operators are used to perform operations on individual bits of numbers.

| Operator | Description                | Example          |
|----------|----------------------------|------------------|
| `&`      | Bitwise AND                 | `a & b`          |
| `|`      | Bitwise OR                  | `a | b`          |
| `^`      | Bitwise XOR                 | `a ^ b`          |
| `~`      | Bitwise Complement          | `~a`             |
| `<<`     | Left Shift                  | `a << 2`         |
| `>>`     | Right Shift                 | `a >> 2`         |

```java
    public class BitwiseExample {
      public static void main(String[] args) {
          int a = 5, b = 3;
          System.out.println("a & b: " + (a & b)); // 1 (Binary: 101 & 011 = 001)
          System.out.println("a | b: " + (a | b)); // 7 (Binary: 101 | 011 = 111)
      }
    }
```

### 6. Unary Operators
Unary operators are used with a single operand to perform various operations like incrementing, decrementing, etc.

| Operator | Description                | Example          |
|----------|----------------------------|------------------|
| `+`      | Unary plus (positive value) | `+a`             |
| `-`      | Unary minus (negative value)| `-a`             |
| `++`     | Increment                   | `a++` or `++a`   |
| `--`     | Decrement                   | `a--` or `--a`   |

```java
  public class UnaryExample {
    public static void main(String[] args) {
        int a = 10;
        System.out.println("a++: " + (a++)); // 10 (then a becomes 11)
        System.out.println("++a: " + (++a)); // 12
        System.out.println("a--: " + (a--)); // 12 (then a becomes 11)
    }
}

```

### 7. Ternary Operator
The ternary operator is a shorthand for the if-else statement and works with three operands. It is also called the conditional operator.

| Operator | Description            | Example                      |
|----------|------------------------|------------------------------|
| `? :`    | Shorthand for if-else   | `condition ? value1 : value2`|


```java
     public class TernaryExample {
        public static void main(String[] args) {
            int a = 10, b = 20;
            int max = (a > b) ? a : b;
            System.out.println("Max value: " + max); // 20
        }
    }

```

## Control Flow Statements
Control flow statements in Java are used to dictate the flow of execution of a program based on certain conditions. The two primary control flow statements you asked for are if-else and switch.

### If-Else Statement
The if-else statement allows you to execute a block of code based on a condition. If the condition evaluates to true, the if block is executed. If the condition is false, the else block (if present) is executed.

Syntax:

```java
     if (condition) {
    // Code to execute if condition is true
    } else {
        // Code to execute if condition is false
    }
```

Example:

```java
     int age = 18;

    if (age >= 18) {
        System.out.println("You are an adult.");
    } else {
        System.out.println("You are a minor.");
    }
```

- Condition: age >= 18 checks if the age is greater than or equal to 18.
- Output: Since the condition is true, it will print: "You are an adult."


**Else-If Ladder:**
You can chain multiple if conditions using else-if to check multiple possibilities.

```java
   int score = 75;

    if (score >= 90) {
        System.out.println("Grade: A");
    } else if (score >= 80) {
        System.out.println("Grade: B");
    } else if (score >= 70) {
        System.out.println("Grade: C");
    } else {
        System.out.println("Grade: F");
    }

```

### Switch Statement
The switch statement provides an alternative to the if-else ladder when there are multiple conditions that depend on the value of a single variable. It is often used when you have many potential values for a variable and want to execute different blocks of code for each value.

Syntax:

```java
    switch (expression) {
    case value1:
        // Code to execute if expression matches value1
        break;
    case value2:
        // Code to execute if expression matches value2
        break;
    // More cases...
    default:
        // Code to execute if none of the cases match
        break;
    }

```
Example : 

```java
   int day = 3;

    switch (day) {
        case 1:
            System.out.println("Monday");
            break;
        case 2:
            System.out.println("Tuesday");
            break;
        case 3:
            System.out.println("Wednesday");
            break;
        default:
            System.out.println("Invalid day");
            break;
    }
```

- Expression: day is evaluated in the switch statement.
- Output: Since day is 3, the output will be: "Wednesday".
- The break statement is used to exit the switch block after a case has been executed, preventing fall-through to the next case.
  
**Switch with Strings (Java 7 and above):**

```java
   String fruit = "apple";

  switch (fruit) {
      case "apple":
          System.out.println("You selected an apple.");
          break;
      case "banana":
          System.out.println("You selected a banana.");
          break;
      default:
          System.out.println("Unknown fruit.");
          break;
  }

```
- Output: Since the string fruit is "apple", it will print: "You selected an apple."

  ### Key Differences Between if-else and switch:
- **Conditions:** if-else checks conditions that return a boolean value, whereas switch compares an expression against a set of constant values.
- **Usage:** switch is usually more efficient when you have many possible values for a single variable, while if-else is more flexible for complex conditions.
- **Types:** In switch, only certain types are allowed (int, char, String, etc.), while if-else can handle any condition.

## Loops
Loops are control structures that allow you to repeatedly execute a block of code as long as a specified condition is true. Java provides three primary types of loops: `for`, `while`, and `do-while`.

### For Loop
The for loop is used when you know in advance how many times you want to iterate. It consists of three parts: initialization, condition, and update.

Syntax:

```java
   for (initialization; condition; update) {
        // Code to execute
    }
```

- Initialization: Initializes the loop control variable.
- Condition: Checks the condition before each iteration. If true, the loop runs; if false, the loop stops.
- Update: Updates the loop control variable after each iteration.
  

```java
  for (int i = 1; i <= 5; i++) {
      System.out.println("Iteration: " + i);
  }
```

Explanation:
- The loop starts with i = 1, checks if i <= 5 (condition), and prints the current value of i.
- After each iteration, i is incremented by 1.
  
Output:

```java
   Iteration: 1
   Iteration: 2
   Iteration: 3
   Iteration: 4
   Iteration: 5
```

### Enhanced For Loop (for-each loop):
- Used to iterate over arrays or collections without using an index.

```java
   int[] numbers = {1, 2, 3, 4, 5};

    for (int num : numbers) {
        System.out.println(num);
    }
```
### While Loop
The while loop checks the condition before executing the loop's body. It continues to iterate as long as the condition remains true.

Syntax:

```java
   while (condition) {
        // Code to execute
    }
```
- Condition: The loop executes as long as this condition evaluates to true.
  
Example:

```java
   int i = 1;

    while (i <= 5) {
        System.out.println("Iteration: " + i);
        i++;
    }
```
Explanation:
- The loop runs as long as i <= 5. After each iteration, i is incremented by 1.
  
Output:

```java
   Iteration: 1
   Iteration: 2
   Iteration: 3
   Iteration: 4
   Iteration: 5
```

### Do-While Loop
The do-while loop is similar to the while loop, but it guarantees at least one iteration because the condition is checked after the loop body is executed.

```java
   do {
        // Code to execute
    } while (condition);
```
Condition: The loop executes the block of code once, then checks the condition. If the condition is `true`, it continues to loop; otherwise, it stops.

Example:

```java
   int i = 1;

    do {
        System.out.println("Iteration: " + i);
        i++;
    } while (i <= 5);
```
Explanation:
- The loop prints the value of i at least once, then checks if i <= 5. If true, it continues to iterate.
  
Output:

```java
   Iteration: 1
   Iteration: 2
   Iteration: 3
   Iteration: 4
   Iteration: 5
```

**Key Difference from while loop:**

In the `do-while` loop, the block of code executes at least once, even if the condition is initially `false`.

### Loop Control Statements
Java also provides loop control statements to alter the normal flow of loops:

- `break:` Exits the loop entirely.
- `continue:` Skips the current iteration and proceeds to the next iteration.
  
  Example with break and continue:

 ```java
      for (int i = 1; i <= 5; i++) {
        if (i == 3) {
            continue; // Skip the current iteration when i is 3
        }
        if (i == 5) {
            break; // Exit the loop when i is 5
        }
        System.out.println("Iteration: " + i);
    }
```
Explanation:
- The continue statement skips the iteration where `i == 3`, so it doesn't print "Iteration: 3".
- The break statement exits the loop when `i == 5`, so the loop stops before it reaches 5.
Output:

 ```java
     Iteration: 1
     Iteration: 2
     Iteration: 4
```

## Arrays
In Java, arrays are fundamental data structures that hold multiple values of the same type. Java provides various utility methods in the java.util.Arrays class to operate on arrays. These methods allow us to perform operations such as sorting, searching, filling, and comparing arrays with ease.

### Declaring and Initializing Arrays
An array is declared by specifying the type of its elements and the array size. You can initialize it at the time of declaration or later.

```java
   int[] numbers = new int[5];  // Declares an array of 5 integers
```
Example 1 : Array of Numbers

```java
   int[] numbers = {1, 2, 3, 4, 5};  // Initializes the array with values
```

Example 2: Array of Strings

```java
    // Declare and initialize an array of strings
    String[] fruits = {"Apple", "Banana", "Orange", "Mango", "Grapes"};
    
    // Accessing elements in the array
    System.out.println(fruits[0]);  // Output: Apple
    System.out.println(fruits[3]);  // Output: Mango
    
    // Looping through the array
    for (String fruit : fruits) {
        System.out.println(fruit);
    }
    
    // Output:
    // Apple
    // Banana
    // Orange
    // Mango
    // Grapes
```
Example 3: Array of Objects

```java
    // Define the Person class
    class Person {
        String name;
        int age;
    
        // Constructor
        Person(String name, int age) {
            this.name = name;
            this.age = age;
        }
    
        // Method to display person details
        void display() {
            System.out.println("Name: " + name + ", Age: " + age);
        }
    }
    
    public class Main {
        public static void main(String[] args) {
            // Declare and initialize an array of Person objects
            Person[] people = new Person[3];
    
            // Initialize each element with a new Person object
            people[0] = new Person("Alice", 30);
            people[1] = new Person("Bob", 25);
            people[2] = new Person("Charlie", 28);
    
            // Access and display the details of each person in the array
            for (Person person : people) {
                person.display();
            }
        }
    }

```
### Common Array Functions from java.util.Arrays

**1. Sorting an Array:** The `Arrays.sort()` method is used to sort arrays in ascending order. It can sort primitive arrays (like `int[]`) and object arrays (like `String[]`).

```java
     import java.util.Arrays;

    int[] numbers = {5, 2, 9, 1, 7};
    Arrays.sort(numbers);  // Sorts the array in ascending order
    System.out.println(Arrays.toString(numbers));  // Output: [1, 2, 5, 7, 9]
```
**2. Binary Search:** The `Arrays.binarySearch()` method is used to search for a specific element in a sorted array. It returns the index of the element if found; otherwise, it returns a negative value.

```java
    int[] numbers = {1, 2, 3, 4, 5};
    int index = Arrays.binarySearch(numbers, 3);
    System.out.println(index);  // Output: 2 (index of element 3)
```
- Note: The array must be sorted before using binarySearch().

**3. Filling an Array:** The `Arrays.fill()` method fills all elements of an array with a specific value.

```java
    int[] numbers = new int[5];
    Arrays.fill(numbers, 10);  // Fills the array with the value 10
    System.out.println(Arrays.toString(numbers));  // Output: [10, 10, 10, 10, 10]
```

**4. Copying Arrays:** The `Arrays.copyOf()` method allows you to create a new array by copying the elements of an existing array.

```java
    int[] original = {1, 2, 3, 4, 5};
    int[] copy = Arrays.copyOf(original, original.length);
    System.out.println(Arrays.toString(copy));  // Output: [1, 2, 3, 4, 5]
```
- You can specify the new array's length in `Arrays.copyOf()`, which allows you to either truncate or extend the original array.

**5. Comparing Arrays:** The Arrays.equals() method checks if two arrays are equal (i.e., have the same length and elements in the same order).

```java
    int[] numbers1 = {1, 2, 3};
    int[] numbers2 = {1, 2, 3};
    boolean areEqual = Arrays.equals(numbers1, numbers2);
    System.out.println(areEqual);  // Output: true
```

**6. Converting Array to String:** The `Arrays.toString()` method returns a string representation of the array.

```java
   int[] numbers = {1, 2, 3, 4, 5};
   System.out.println(Arrays.toString(numbers));  // Output: [1, 2, 3, 4, 5]
```

**7. Converting Multi-dimensional Arrays to String:** For multi-dimensional arrays, you can use Arrays.deepToString() to get a string representation.

```java
  int[][] matrix = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
  System.out.println(Arrays.deepToString(matrix));  // Output: [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

**8. Copying Part of an Array:** The `Arrays.copyOfRange()` method allows copying a portion of an array.

```java
  int[] original = {1, 2, 3, 4, 5};
  int[] partialCopy = Arrays.copyOfRange(original, 1, 4);
  System.out.println(Arrays.toString(partialCopy));  // Output: [2, 3, 4]
```

**9. Parallel Sorting:** The Arrays.parallelSort() method sorts large arrays more efficiently by using multiple threads in parallel.

```java
  int[] numbers = {9, 4, 6, 1, 7};
  Arrays.parallelSort(numbers);
  System.out.println(Arrays.toString(numbers));  // Output: [1, 4, 6, 7, 9]
```

**10. Checking if Two Multi-dimensional Arrays are Equal:** For multi-dimensional arrays, `Arrays.deepEquals()` checks for deep equality.

```java
  int[][] matrix1 = {{1, 2}, {3, 4}};
  int[][] matrix2 = {{1, 2}, {3, 4}};
  boolean areEqual = Arrays.deepEquals(matrix1, matrix2);
  System.out.println(areEqual);  // Output: true
```

### Summary of Common Arrays Functions

| **Function**                           | **Description**                                | **Example**                           |
|----------------------------------------|------------------------------------------------|---------------------------------------|
| `sort(array)`                          | Sorts the array in ascending order             | `Arrays.sort(array);`                 |
| `binarySearch(array, key)`             | Searches for key in a sorted array             | `Arrays.binarySearch(array, 3);`      |
| `fill(array, value)`                   | Fills the entire array with value              | `Arrays.fill(array, 0);`              |
| `copyOf(array, length)`                | Copies the array into a new array              | `Arrays.copyOf(array, 5);`            |
| `equals(array1, array2)`               | Checks if two arrays are equal                 | `Arrays.equals(arr1, arr2);`          |
| `toString(array)`                      | Converts the array to a string                 | `Arrays.toString(array);`             |
| `deepToString(array)`                  | Converts a multi-dimensional array to a string | `Arrays.deepToString(matrix);`        |
| `copyOfRange(array, start, end)`       | Copies a range of the array                    | `Arrays.copyOfRange(arr, 0, 3);`      |
| `parallelSort(array)`                  | Sorts the array using multiple threads         | `Arrays.parallelSort(arr);`           |
| `deepEquals(array1, array2)`           | Checks if two multi-dimensional arrays are equal| `Arrays.deepEquals(matrix1, matrix2);`|

### Difference between Table and ArrayList in Java

In Java, a **Table** (often referring to two-dimensional arrays or hash tables) and an **ArrayList** have distinct characteristics and purposes. Here's a breakdown of their key differences:

| **Feature**            | **Table (2D Array or HashTable)**                                                                 | **ArrayList**                                                                                 |
|------------------------|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| **Type**               | Array (fixed-size) or `HashTable` (for key-value pairs).                                          | Dynamic array (part of Java's `List` interface, resizable).                                   |
| **Size**               | Fixed at the time of creation (for arrays).                                                       | Resizable, grows or shrinks dynamically.                                                      |
| **Data Structure**     | 2D Array: Static array structure.<br>HashTable: Key-value pair structure.                         | Implements a dynamic array, can grow or shrink as needed.                                     |
| **Performance**        | Accessing elements by index is very fast (O(1) for arrays).                                       | Accessing elements is also O(1), but resizing operations (like adding elements) take O(n).    |
| **Storage Type**       | Stores elements of the same data type (for arrays).                                               | Can store objects of any data type (generic, `ArrayList<Type>`).                              |
| **Memory Allocation**  | Memory is allocated at the time of creation and cannot be changed for arrays.                     | Memory is allocated dynamically and expands when needed.                                      |
| **Efficiency**         | Fixed-size, hence less memory overhead (arrays).                                                  | More flexible, but resizing may involve overhead (copying elements to a new larger array).     |
| **Type Safety**        | Arrays are strongly typed, meaning the data type of elements is fixed at compile time.            | ArrayList is generic, meaning you can define the type (`ArrayList<String>`, `ArrayList<Integer>`, etc.). |
| **Multi-dimensional**  | Arrays can be multi-dimensional (e.g., 2D or 3D arrays).                                          | ArrayLists are single-dimensional, but can contain other lists to simulate multidimensional arrays. |
| **Initialization**     | Arrays must be initialized with a fixed size when created (e.g., `int[3][3]` or `new int[5]`).    | ArrayList grows dynamically as elements are added (e.g., `new ArrayList<Integer>()`).          |
| **Methods and Utilities** | Arrays have limited built-in methods. (Use `Arrays` class for utility methods like sorting).   | ArrayList has built-in methods such as `add()`, `remove()`, `size()`, `clear()`, etc.         |
| **Null Values**        | Can contain `null` values (for arrays and hash tables).                                           | Can also contain `null` values in `ArrayList`.                                                |

### Key Points:

#### **Table (2D Array or HashTable)**
1. **2D Array Example**: 
   - A table in Java can refer to a two-dimensional array, where each "row" is an array, and each "column" contains elements of the same type.
   - Example:
     
     ```java
       int[][] table = {
           {1, 2, 3},
           {4, 5, 6},
           {7, 8, 9}
       };
     ```

2. **HashTable Example**:
   - A `HashTable` is a collection of key-value pairs that maps keys to values. It is synchronized, but largely replaced by `HashMap` due to better performance.
   - Example:
     
     ```java
       Hashtable<String, Integer> hashtable = new Hashtable<>();
       hashtable.put("Alice", 30);
       hashtable.put("Bob", 25);
     ```

#### **ArrayList**
- An `ArrayList` is a resizable array in Java, which allows dynamic memory allocation. It can store objects of any type using generics and has built-in methods for common operations (e.g., adding, removing elements).
  
- Example:
  
   ```java
       ArrayList<String> fruits = new ArrayList<>();
       fruits.add("Apple");
       fruits.add("Banana");
       fruits.add("Orange");
       
       System.out.println(fruits.get(0)); // Output: Apple
    ```

## String Manipulation
  
Strings in Java are objects that represent sequences of characters. Java provides a variety of built-in methods for manipulating strings. Here are some common operations for string manipulation:


### 1. Creating Strings
Strings can be created using string literals or the String constructor:

 ```java
     String str1 = "Hello, World!"; // String literal
     String str2 = new String("Hello, World!"); // String constructor
  ```

### 2. Common String Methods

| **Method**                     | **Description**                                      | **Example**                                         |
|--------------------------------|------------------------------------------------------|-----------------------------------------------------|
| `length()`                     | Returns the length of the string.                    | `str1.length();`  // Returns 13                     |
| `charAt(int index)`           | Returns the character at the specified index.        | `str1.charAt(0);`  // Returns 'H'                   |
| `substring(int beginIndex)`    | Returns a substring starting from the specified index. | `str1.substring(7);` // Returns "World!"            |
| `substring(int beginIndex, int endIndex)` | Returns a substring from the specified range. | `str1.substring(0, 5);` // Returns "Hello"          |
| `indexOf(String str)`         | Returns the index of the first occurrence of the specified substring. | `str1.indexOf("World");` // Returns 7          |
| `lastIndexOf(String str)`     | Returns the index of the last occurrence of the specified substring. | `str1.lastIndexOf("o");` // Returns 8          |
| `toLowerCase()`               | Converts all characters to lowercase.                 | `str1.toLowerCase();` // Returns "hello, world!"   |
| `toUpperCase()`               | Converts all characters to uppercase.                 | `str1.toUpperCase();` // Returns "HELLO, WORLD!"   |
| `trim()`                      | Removes leading and trailing whitespace.              | `str1.trim();` // Removes spaces if present         |
| `replace(char oldChar, char newChar)` | Replaces occurrences of a character with another. | `str1.replace('o', 'a');` // Returns "Hella, Warld!" |
| `split(String regex)`         | Splits the string into an array based on a regex.     | `str1.split(",");` // Returns array `["Hello", " World!"]` |
| `startsWith(String prefix)`    | Checks if the string starts with the specified prefix. | `"Java".startsWith("Ja");` // Returns `true`        |
| `endsWith(String suffix)`      | Checks if the string ends with the specified suffix.  | `"Java".endsWith("va");` // Returns `true`          |
| `contains(CharSequence seq)`   | Checks if the string contains the specified sequence. | `"Java".contains("av");` // Returns `true`          |
| `equalsIgnoreCase(String str)` | Compares two strings, ignoring case differences.      | `"java".equalsIgnoreCase("Java");` // Returns `true`|
| `isEmpty()`                    | Checks if the string is empty (length = 0).           | `"".isEmpty();` // Returns `true`                   |
| `join(CharSequence delimiter, CharSequence... elements)` | Joins multiple strings with a delimiter. | `String.join("-", "2023", "10", "05");` // Returns `"2023-10-05"` |
| `matches(String regex)`        | Checks if the string matches a regular expression.    | `"abc123".matches("[a-z]+[0-9]+");` // Returns `true`|
| `replaceAll(String regex, String replacement)` | Replaces all matches of a regex with a replacement. | `"abc123".replaceAll("\\d", "#");` // Returns `"abc###"` |
| `replaceFirst(String regex, String replacement)` | Replaces the first match of a regex with a replacement. | `"abc123".replaceFirst("\\d", "#");` // Returns `"abc#23"` |
| `repeat(int count)`            | Repeats the string a specified number of times.       | `"Hello".repeat(3);` // Returns `"HelloHelloHello"`|
| `strip()`                      | Removes leading and trailing whitespace (introduced in Java 11). | `"  Hello  ".strip();` // Returns `"Hello"`        |
| `stripLeading()`               | Removes leading whitespace only.                     | `"  Hello  ".stripLeading();` // Returns `"Hello  "`|
| `stripTrailing()`              | Removes trailing whitespace only.                    | `"  Hello  ".stripTrailing();` // Returns `"  Hello"`|
| `compareTo(String anotherString)` | Compares two strings lexicographically.            | `"abc".compareTo("def");` // Returns a negative number |
| `concat(String str)`           | Concatenates the specified string to the end of the current string. | `"Hello".concat(" World");` // Returns `"Hello World"` |
| `codePointAt(int index)`       | Returns the Unicode code point at the specified index.| `"A".codePointAt(0);` // Returns `65` (Unicode for 'A') |
| `intern()`                     | Returns a canonical representation of the string.    | `"Hello".intern();` // Interns the string for memory efficiency|



### 3. Concatenating Strings

Strings can be concatenated using the `+` operator or the `concat()` method:

 ```java
    String firstName = "John";
    String lastName = "Doe";
    String fullName = firstName + " " + lastName; // Using + operator
    // or
    String fullName2 = firstName.concat(" ").concat(lastName); // Using concat() method
  ```

### 4. StringBuilder and StringBuffer

For more efficient string manipulation, especially in loops, it’s better to use StringBuilder or StringBuffer:

- **StringBuilder:** Not synchronized, faster for single-threaded operations.
- **StringBuffer:** Synchronized, thread-safe but slower than StringBuilder.
  
Example of StringBuilder:

 ```java
     StringBuilder sb = new StringBuilder();
    sb.append("Hello");
    sb.append(", ");
    sb.append("World!");
    String result = sb.toString(); // Returns "Hello, World!"
  ```

### 5. Formatting Strings

You can format strings using the `String.format()` method or `System.out.printf()` for console output:

 ```java
     String name = "Alice";
    int age = 30;
    String formatted = String.format("%s is %d years old.", name, age); // Returns "Alice is 30 years old."
    System.out.println(formatted);
  ```

### 6. Checking String Equality
Strings can be compared using the `equals()` method or `equalsIgnoreCase()` for case-insensitive comparisons:

 ```java
    String strA = "Hello";
    String strB = "hello";
    boolean isEqual = strA.equals(strB); // Returns false
    boolean isEqualIgnoreCase = strA.equalsIgnoreCase(strB); // Returns true
  ```

### 7. Extracting String
The substring() method in Java is used to extract a portion of a string based on specified indices. There are two common forms of the method:

- `substring(int beginIndex):` Returns a substring starting from the given index up to the end of the string.
- `substring(int beginIndex, int endIndex):` Returns a substring starting from the `beginIndex` and ending right before the `endIndex` (exclusive of endIndex).

Example:

 ```java
     public class SubstringExample {
      public static void main(String[] args) {
          String str = "Hello, World!";
  
          // Example 1: Using substring(int beginIndex)
          String result1 = str.substring(7);
          System.out.println(result1);  // Output: World!
  
          // Example 2: Using substring(int beginIndex, int endIndex)
          String result2 = str.substring(0, 5);
          System.out.println(result2);  // Output: Hello
  
          // Example 3: Extracting a portion of the string
          String result3 = str.substring(7, 12);
              System.out.println(result3);  // Output: World
          }
      }
  ```
- `str.substring(7)` extracts the substring starting from index `7`, which is `"World!"`.
- `str.substring(0, 5)` extracts characters from index `0` to `4` (excluding `5`), which is `"Hello"`.
- `str.substring(7, 12)` extracts characters from index `7` to `11`, resulting in `"World"`.

# Java 8 Basics
 ## 1. Lambda Expressions
  **Zero Parameters :**
  
  ```java
  () -> System.out.println("No parameters!");
  ```

 **One Parameter :**
  
  ```java
  s -> System.out.println(s);
  ```

 **Multiple Parameters :**
  
  ```java
  (int x, int y) -> x + y;
  ```

 **Single Expression :**
  
  ```java
  a -> a * a // no need for the return keyword
  ```

  **Code Block :**
  
  ```java
 (a , b) -> { return a + b }; // Multiple statements inside braces
  ```
  
  ## 2. Functional Interfaces
  - A functional interface is an interface that contains only `one abstract method`. It can also contain `default` and `static` methods, but it must have exactly one abstract method.
  - The `@FunctionalInterface` notation is optional but recommended to clearly indicate to other developers that this interface is intended to be used as a functional interface. If you try to declare a second abstract method in an interface annotated with `@FunctionalInterface` , the compiler will generate an error.
    
   ```java
        @FunctionalInterface
        interface MyFunctionalInterface {
            void myAbstractMethod();
        
            // This line would generate an error because it introduces a second abstract method
            // void anotherAbstractMethod();
            
            // This is a default method
            default void myDefaultMethod() {
                System.out.println("This is a default method.");
            }
        
            // This is a static method
            static void myStaticMethod() {
                System.out.println("This is a static method.");
            }
        }
   ```

   ```java
       public class Main {
          public static void main(String[] args) {
              // Using a lambda expression to implement the abstract method of the functional interface
              MyFunctionalInterface myInstance = () -> System.out.println("Implementation of myAbstractMethod.");
              
              // Calling the abstract method
              myInstance.myAbstractMethod(); // Output: "Implementation of myAbstractMethod."
              
              // Calling the default method
              myInstance.myDefaultMethod(); // Output: "This is a default method."
              
              // Calling the static method
              MyFunctionalInterface.myStaticMethod(); // Output: "This is a static method."
          }
       }
   ```

  ### Functional Interface with Lambda Expression
  
   ```java
      import java.util.function.BinaryOperator;

        public class Main {
          public static void main(String[] args) {
      
              // Lambda expression for multiplying two numbers
              BinaryOperator<Integer> multiplication = (a, b) -> a * b;
              int result1 = multiplication.apply(5, 3); // result1 will be 15
      
              // Custom functional interface with an instance main method
              Operation subtraction = (a, b) -> a - b;
              int result3 = subtraction.operate(10, 3); // result3 will be 7
      
              Operation division = (a, b) -> a / b;
              int result4 = division.operate(15, 5); // result4 will be 3
      
              System.out.println("Multiplication: " + result1);
              System.out.println("Subtraction: " + result3);
              System.out.println("Division: " + result4);
              }
            }
            
            // Custom functional interface with an instance main method
            @FunctionalInterface
            interface Operation {
                int operate(int a, int b);
           }
   ```
    
  ### Functional Interface with Method Reference (Methode Instance)
  - `Method Reference:` A method reference is a shorthand notation for invoking a method or passing it as a parameter. It provides a way to refer to a method without executing it directly, typically by using the `::` operator followed by the method name. Method references are often used in functional.
    
  ```java
    import java.util.function.BinaryOperator;
    import java.util.function.UnaryOperator;

      public class Main {
        public static void main(String[] args) {
    
            // Using a method reference for addition
            BinaryOperator<Integer> addition = Main::add;
            int result2 = addition.apply(10, 5); // result2 will be 15
  
            System.out.println("Addition: " + result2);

            // Using a method reference for conversion to upper case
            UnaryOperator<String> toUpperCase = String::toUpperCase;
            String upperCaseString = toUpperCase.apply("hello"); // upperCaseString will be "HELLO"
    
            System.out.println("Uppercase String: " + upperCaseString);
            }
    
              // Static method for addition
              static int add(int a, int b) {
                  return a + b;
              }
          }
  ```

  ### Predicate interface
  - `Predicate interface` is a functional interface that represents a function that takes an argument and returns a `boolean` value, often used for testing a condition. This Predicate interface is widely used in the context of lambda expressions and methods of the Stream class to perform filtering or selecting elements.
    
  ```java
      import java.util.function.Predicate;

      public class Main {
          public static void main(String[] args) {

              // Using a pre-defined functional interface (Predicate) for checking even numbers
              Predicate<Integer> isEven = num -> num % 2 == 0;
              boolean result = isEven.test(10); // result will be true

              System.out.println("Is 10 even? " + result);
      
              // Using a Predicate for string comparison
              Predicate<String> test = tes -> "toto".equals(tes);
              boolean result = test.test("toto");

              System.out.println("Is the string 'toto'? " + result); // result will be true
          }
      }
  ```
## 3. Static and Default Method in Interface

- `Static method` within an interface is a method that can be called directly on the interface itself, without requiring an instance of a class that implements the interface. Static methods in interfaces were introduced in Java 8 along with default methods.
  
- `Default method` is a method defined within an interface with a default implementation. Prior to the introduction of default methods in Java 8, interfaces could only contain method signatures, meaning methods without bodies. With default methods, it became possible to provide a default implementation for methods within interfaces.
  
  ```java
       interface MyInterface {
          void abstractMethod(); // Abstract method
      
          default void defaultMethod() { // Default method
              System.out.println("This is a default method.");
          }
      
          static void staticMethod() { // Static method
              System.out.println("This is a static method.");
          }
      }
  ```
  
  ```java
      class MyClass implements MyInterface {
          public void abstractMethod() {
              System.out.println("Implementing the abstract method.");
          }
      }
  ```
  ```java
      public class Main {
        public static void main(String[] args) {
            MyClass obj = new MyClass();
            obj.abstractMethod(); // Calling the abstract method
            obj.defaultMethod();  // Calling the default method
            MyInterface.staticMethod(); // Calling the static method directly on the interface
        }
    }
   ```
  ## 4. Collections Interfaces
    
    Collection Interfaces refers to the interfaces provided in the Java Collections Framework (JCF) that define various types of collections. These interfaces are part of the java.util   package and provide a standardized way of working with collections of objects.
    
    ![Java-Collections-Framework-Hierarchy](https://github.com/douaeelh2/Java-Documentation/assets/127549220/2837ac14-8fc7-41a8-b72c-680fe454136d)
  
   ### Collection:
    - This is the root interface in the collection hierarchy. It defines basic operations applicable to all collections such as adding, removing, and querying elements. Use this when you need a general-purpose collection to store a group of objects without caring about the specific order or uniqueness of elements.
        
       ```java
          import java.util.ArrayList;
          import java.util.Collection;
          
          public class Main {
              public static void main(String[] args) {
                  Collection<String> names = new ArrayList<>();
          
                  names.add("Alice");
                  names.add("Bob");
                  names.add("Charlie");
          
                  System.out.println("Collection : " + names); //Output : Collection : [Alice, Bob, Charlie]
              }
          }
  
       ```
       
   ### List:
     - An ordered collection (sometimes called a sequence). Lists allow duplicate elements and provide methods for accessing elements by their index. Common implementations of the List interface include `ArrayList`, `LinkedList` , etc.
    
       ```java
          import java.util.ArrayList;
          import java.util.List;
          
          public class ListExample {
              public static void main(String[] args) {
                  List<Integer> numbers = new ArrayList<>();
                  
                  numbers.add(10);
                  numbers.add(20);
                  numbers.add(30);
                  
                  System.out.println("List: " + numbers); //Output : List: [10, 20, 30]
                  
                  // Accessing an element by its index
                  int secondElement = numbers.get(1);
                  System.out.println("Second element: " + secondElement);  //Output : Second element: 20
              }
          }
  
       ```
  
   ### Map:
    - A map is a collection that associates unique keys with corresponding values. Each key is unique and corresponds to a single value. Common implementations of the Map interface include:
      - `HashMap:` This class uses a hash table to store key-value pairs, providing fast lookup and access. However, the order of elements is not guaranteed.
        
        ```java
          import java.util.HashMap;
          import java.util.Map;
        
            public class Main {
                public static void main(String[] args) {
                    Map<String, Integer> hashMap = new HashMap<>();
            
                    hashMap.put("John", 25);
                    hashMap.put("Alice", 30);
                    hashMap.put("Bob", 20);
            
                    for (Map.Entry<String, Integer> entry : hashMap.entrySet()) {
                        System.out.print(entry.getKey() + " - " + entry.getValue());
                        System.out.print("  ");  //Output : Bob - 20  Alice - 30  John - 25
                    }
                }
            }
        ```
      - `TreeMap:` This class implements the SortedMap interface and uses a red-black tree to store key-value pairs. Elements are sorted according to the natural order of keys or using a comparator provided when creating the TreeMap object.
        
        ```java
           import java.util.TreeMap;
           import java.util.Map;
        
           public class Main {
              public static void main(String[] args) {
                  Map<String, Integer> treeMap = new TreeMap<>();
          
                  treeMap.put("John", 25);
                  treeMap.put("Alice", 30);
                  treeMap.put("Bob", 20);
          
                  for (Map.Entry<String, Integer> entry : treeMap.entrySet()) {
                      System.out.print(entry.getKey() + " - " + entry.getValue());
                    System.out.print("  "); //Output : Alice - 30  Bob - 20  John - 25
                  }
              }
          }
        ```
      - `LinkedHashMap:` This class maintains the insertion order of elements in addition to providing fast access to elements through a hash table. This means that elements are traversed in insertion order when iterating over the map.
  
    ### Set:
    - A set is a collection that does not allow duplicate elements. This means that each element in a set is unique. Common implementations of the Set interface include HashSet, TreeSet, LinkedHashSet, etc.
      
      `HashSet:`
      - It is implemented using a hash table. It does not maintain any order of elements; instead, it uses the hash code of the objects to store elements.
      -  If you try to add duplicates, they will be ignored.
      -  Allows a single null element.
       
           ```java
              import java.util.HashSet;
              import java.util.Set;
           
              public class Main {
                  public static void main(String[] args) {
                      Set<String> hashSet = new HashSet<>();
                      hashSet.add("banana");
                      hashSet.add("apple");
                      hashSet.add("orange");
                      hashSet.add("banana");
              
                      System.out.print("Elements in HashSet:");
                      for (String fruit : hashSet) {
                          System.out.print(fruit); //Output : Elements in HashSet: banana  orange  apple
                      }
                  }
              }
           ```
           
      `TreeSet:`
      - It is implemented using a red-black tree. It stores elements in sorted order (either natural ordering or specified by a comparator).
      -  Also does not allow duplicate elements.
      -  Does not allow null elements. If you try to add a null element, it will throw a NullPointerException.
       
           ```java
              import java.util.TreeSet;
              import java.util.Set;
           
              public class Main {
                  public static void main(String[] args) {
                      Set<String> treeSet = new TreeSet<>();
                      treeSet.add("banana");
                      treeSet.add("apple");
                      treeSet.add("orange");
                      treeSet.add("banana");
              
                      System.out.print("Elements in TreeSet:");
                      for (String fruit : treeSet) {
                          System.out.print(fruit);  //Output : Elements in TreeSet: apple  banana  orange
                      }
                  }
              }
           ```
           
      - `LinkedHashSet:` This class maintains the insertion order of elements in addition to providing fast access to elements through a hash table. This means that elements are traversed in insertion order when iterating over the map.

    ## 5. Stream API
    Stream API is a way to express and process collections of objects. Enable us to perform operations like filtering, mapping,reducing and sorting. The Stream API in the `java.util.stream` package in Java offers an simple approach to describe operations to be executed on a dataset.
  
   ![Stream-in-Java-768](https://github.com/douaeelh2/Java-Documentation/assets/127549220/dff08118-d389-4aeb-adfc-fe114b78bdc0)
    
     ### Java Stream Creation
    - Obtain a stream from an existing array:
      
    ```java
       private static Employee[] arrayOfEmps = {
          new Employee(1, "Jeff Bezos", 100000.0), 
          new Employee(2, "Bill Gates", 200000.0), 
          new Employee(3, "Mark Zuckerberg", 300000.0)
        };
        Stream.of(arrayOfEmps);
    ```
    - Obtain a stream from an existing list:
      
    ```java
       private static List<Employee> empList = Arrays.asList(arrayOfEmps);
      empList.stream();
    ```
    
    - Create a stream from individual objects:
      
    ```java
       Stream.of(arrayOfEmps[0], arrayOfEmps[1], arrayOfEmps[2]);
    ```
    
    - Create a stream using Stream.builder():
      
    ```java
        Stream.Builder<Employee> empStreamBuilder = Stream.builder();
        empStreamBuilder.accept(arrayOfEmps[0]);
        empStreamBuilder.accept(arrayOfEmps[1]);
        empStreamBuilder.accept(arrayOfEmps[2]);
        Stream<Employee> empStream = empStreamBuilder.build();
    ```

    ### Java Stream Operations
    **Intermediate Operations:** <br>
    - `filter():` Returns a Stream containing only the elements that satisfy a specific condition.
      
      ```java
          List<String> fruits = Arrays.asList("apple", "banana", "orange");
          Stream<String> result = fruits.stream().filter(s -> s.startsWith("a"));
          System.out.println(result); // Output : apple
      ```
      
    - `map():` Transforms each element of the Stream into another element by applying a specified function.
      
      ```java
          List<String> fruits = Arrays.asList("apple", "banana", "orange");
          Stream<Integer> result = fruits.stream().map(String::length);
          System.out.println(result); // prints the length of each element of the fruits list
      ```
      
    - `distinct():` Returns a Stream with distinct elements (removes duplicates).
      
      ```java
          List<String> numbers = Arrays.asList("1", "2", "2", "3", "4", "4");
          Stream<String> result = numbers.stream().distinct();
          result.forEach(System.out::println);  // Output : 1 2 3 4
      ```
    - `reduce():` Reduces the elements of the Stream using a specific associative operation (e.g., sum, product, concatenation, etc.).
      
      ```java
          List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
          Optional<Integer> sum = numbers.stream()
                                         .reduce((a, b) -> a + b);
          sum.ifPresent(System.out::println); // Output: 15 (1 + 2 + 3 + 4 + 5)  
      ```

    - `sorted():` Sorts the elements of the Stream.
      
      ```java
          List<Integer> numbers = Arrays.asList(3, 1, 4, 1, 2);
          Stream<Integer> result = numbers.stream().sorted();
          result.forEach(System.out::println); // Output : 1 1 2 3 4
      
      ```
      
    - `flatMap():` Transforms each element of the Stream into a Stream of other elements, then flattens the resulting streams into a single Stream.
      
      ```java
          List<List<Integer>> listOfLists = Arrays.asList(
                Arrays.asList(1, 2, 3),
                Arrays.asList(4, 5, 6),
                Arrays.asList(7, 8, 9)
            );
          List<Integer> flattenedList = listOfLists.stream()
                                                    .flatMap(List::stream)
                                                    .collect(Collectors.toList());
          System.out.println(flattenedList);  // Output : [1, 2, 3, 4, 5, 6, 7, 8, 9]
      ```
      
    - `skip():` Skips the specified number of elements from the beginning of the Stream.
       
       ```java
          List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);
          List<Integer> skippedNumbers = numbers.stream()
                                                .skip(5)
                                                .collect(Collectors.toList());
          System.out.println(skippedNumbers); // Output: [6, 7, 8, 9, 10]
       ```
       
   - `limit():` Limits the size of the Stream to the specified number of elements.

      ```java
          List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);
          List<Integer> skippedNumbers = numbers.stream()
                                                .skip(5)
                                                .collect(Collectors.toList());
          System.out.println(skippedNumbers); // Output: [6, 7, 8, 9, 10]
       ```

    **Terminal Operations:** <br>
    - `forEach():` Performs an action for each element of the stream.
      
      ```java
          List<String> fruits = Arrays.asList("apple", "banana", "orange");
          fruits.stream().forEach(System.out::println);//prints each element of the list
      ```

    - `collect():` Collects the elements of the Stream into a specific data structure (e.g., a list, set, map, etc.).
           
      ```java
          List<String> names = Arrays.asList("Alice", "Bob", "Charlie", "David");
          List<String> modifiedNames = names.stream()
                    .filter(name -> name.length() > 4)
                    .map(String::toUpperCase)
                    .collect(Collectors.toList());//collect the result into a list
      ```
# Java 11 Basics
 ## 1. New String Methods 
  - `isBlank():` method was introduced in Java 11 in the java.lang.String class. It allows you to check if a string is empty or contains only whitespace characters.It returns true if the string is empty or contains only whitespace characters and false if the string contains at least one non-whitespace character.

    ```java
        public class IsBlankExample {
            public static void main(String[] args) {
                String str1 = ""; // Empty string
                String str2 = "    "; // String containing only whitespace characters
                String str3 = "Hello"; // String containing non-whitespace characters
                String str4 = "   Hello   "; // String containing whitespace characters along with text
        
                System.out.println("str1 is blank: " + str1.isBlank()); // true
                System.out.println("str2 is blank: " + str2.isBlank()); // true
                System.out.println("str3 is blank: " + str3.isBlank()); // false
                System.out.println("str4 is blank: " + str4.isBlank()); // false
            }
          }
           
    ```
 - `strip():` removes leading and trailing whitespace from a string.
     
      ```java  
          String trimmedStr = "   Hello, world!   ".strip();
          System.out.println(trimmedStr); // Output : "Hello, world!" 
      ```
 - `repeat():` repeats a string a certain number of times.
     
      ```java  
         String repeatedStr = "Java ".repeat(3);
         System.out.println(repeatedStr); // Output: "Java Java Java "
      ```
      
 ## 2. HttpClient API : 
 - `HttpClient:` This API provides a modern alternative to the older HttpURLConnection class and offers richer features for making synchronous or asynchronous HTTP requests, handling cookies, headers, etc. It is built on the concept of reactive streams, making it more flexible and performant in scenarios where many requests need to be handled efficiently.
   
     ```java
        import java.io.IOException;
        import java.net.URI;
        import java.net.http.HttpClient;
        import java.net.http.HttpRequest;
        import java.net.http.HttpResponse;
        
        public class Main {
            public static void main(String[] args) throws IOException, InterruptedException {

                // Create an HttpClient
                HttpClient client = HttpClient.newHttpClient();
     
                // Specify the URL for the GET request
                String url = "https://jsonplaceholder.typicode.com/posts/1";
                HttpRequest request = HttpRequest.newBuilder()
                        .uri(URI.create(url))
                        .GET()
                        .build();
     
                // Send the GET request and retrieve the response
                HttpResponse<String> response = client.send(request, HttpResponse.BodyHandlers.ofString());
                System.out.println("Status code: " + response.statusCode());
                System.out.println("Response body: " + response.body());
            }
        }
     ```   

# Java OOP (Object-Oriented Programming)
 ## 1. Encapsulation 
   - `Encapsulation` is the mechanism of bundling the data `(attributes)` and the methods `(functions)` that operate on the data into a single unit called a class.
   -  It allows data to be hidden from the outside world and accessed only through the methods defined in the class.
     
     
   ```java
   public class Car {
    private String model;
    private int year;
    
    // Constructor
    public Car(String model, int year) {
        this.model = model;
        this.year = year;
    }
    
    // Getter methods
    public String getModel() {
        return model;
    }
    
    public int getYear() {
        return year;
    }
    
    // Setter methods
    public void setModel(String model) {
        this.model = model;
    }
    
    public void setYear(int year) {
        this.year = year;
    }
   }
   ```
   
 ## 2. Inheritance
   - `Inheritance` is a mechanism in which a new class inherits properties and behavior `(methods)` from an existing class.
   - Promoting code reuse, class hierarchy, and object specialization.

   ```java
    // Parent class
class Vehicle {
    String brand;

    void drive() {
        System.out.println("Driving a vehicle...");
    }
}
 ```

 ```java

// Child class inheriting from Vehicle
class Car extends Vehicle {
    int numberOfSeats;

    void accelerate() {
        System.out.println("Car is accelerating...");
    }
}
 ```

 ```java

// Main class
public class Main {
    public static void main(String[] args) {
        // Creating an instance of Car
        Car myCar = new Car();
        myCar.brand = "Toyota";
        myCar.numberOfSeats = 5;

        // Accessing methods from both Vehicle and Car
        myCar.drive(); // Inherited from Vehicle class
        myCar.accelerate(); // Specific to Car class
    }
}

```
 ## 3. Abstraction
   - `Abstraction` is the process of hiding the implementation details and showing only the essential features of an object. It helps in reducing programming complexity and focusing on relevant aspects
   - `Abstract class` cannot be instantiated on their own and may contain abstract methods (methods without implementation)
     
```java
  // Abstract class
abstract class Shape {
    abstract void draw(); // Abstract method
}
```

```java
// Concrete class implementing Shape
class Circle extends Shape {
    void draw() {
        System.out.println("Drawing a circle");
    }
}
```
## 4. Polymorphism
  - `Polymorphism` is the ability of an object to take on different forms or behaviors depending on the context in which it is used. There are two main types of polymorphism in Java: `compile-time polymorphism` (also known as `method overloading`) and `runtime polymorphism` (also known as `method overriding`).

 ### 1. Method overloading polymorphism (or interface polymorphism):

 - This occurs when there are multiple methods with the same name within the same class, but with different parameter lists (signature).
 - The Java compiler determines which method to call based on the number and types of arguments passed to the method.
 - Method overloading is an example of compile-time polymorphism.
    
  ```java
     class Calculator {
      public int add(int a, int b) {
          return a + b;
      }
      
      public double add(double a, double b) {
          return a + b;
          }
      }
 ```

 ```java
    public class Main {
        public static void main(String[] args) {
            Calculator calculator = new Calculator();
            System.out.println(calculator.add(1, 2)); // Calls the add(int, int) method
            System.out.println(calculator.add(1.5, 2.5)); // Calls the add(double, double) method
        }
    }
 ```


  ### 2. Subtype polymorphism (or inheritance polymorphism):
 - This occurs when a method in a subclass has the same signature (name and parameter list) as a method in its superclass.
 - When the method is called on an object of the subclass, the Java Virtual Machine (JVM) determines at runtime which version of the method to execute based on the actual type of the object.
 - It is based on the actual type of object being referred to by the reference variable, not on the type of the reference variable itself.
 - Method overriding is an example of runtime polymorphism.
    
  ```java

    class Animal {
    public void makeSound() {
        System.out.println("Animal makes a sound");
        }
    }
    
    class Dog extends Animal {
        @Override
        public void makeSound() {
            System.out.println("Dog barks");
        }
    }
  
  ```

  ```java
      public class Main {
          public static void main(String[] args) {
              Animal animal = new Dog(); // Polymorphism
              animal.makeSound(); // Calls makeSound from Dog class
          }
      }

  ```
 ## 5. Aggregation and Composition
  - `Aggregation` represents a "has-a" relationship.
  - It occurs when an object contains another object, but the contained object can exist independently of the container object.

   ```java
       class Department {
       private String name;
       // Other attributes and methods
       
       // Aggregation: Department has-a Professor
       private Professor[] professors; // Array of professors
   
       public Department(String name) {
           this.name = name;
           professors = new Professor[10]; // Example: department can have up to 10 professors
       }
       
       // Other methods to manage professors
   }
   
   class Professor {
       private String name;
       // Other attributes and methods
       
       public Professor(String name) {
           this.name = name;
       }
   }

  ```
In this example, a `Department` has multiple `Professor` objects. However, the `Professor` objects can exist independently of the`Department`. If the `Department` object is destroyed, the `Professor` objects still exist.

  - `Composition` represents a stronger form of aggregation and implies a "part-of" relationship.
  - In composition, the lifetime of the contained object is dependent on the lifetime of the container object.
    
       ```java
        class Car {
         // Composition: Car has-a Engine
         private Engine engine;
     
         public Car() {
             this.engine = new Engine(); // Engine is created along with the Car
         }
         
           // Other attributes and methods
       }
       
       class Engine {
           // Attributes and methods of Engine
       }

     ```
 In this example, a `Car` is composed of an `Engine`. The Engine object is created along with the `Car` object and cannot exist independently. If the `Car` object is destroyed, the `Engine` object is also destroyed.

 ## 6. Interface & Class
 
  - `Interface` is a reference type, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types.
  - All methods declared in an interface are implicitly `public` and `abstract`. They cannot contain methods with implementation.
  - Classes that implement an interface must provide an `implementation` for all methods declared in that interface.
  - A class can implement `multiple interfaces`, thus providing increased flexibility in program design.
  - Interfaces can be used to define types, enabling `polymorphism`.
  - Extend one or more interfaces

  ```java
       // Define an interface
      interface Animal {
          void eat(); // method signature
          void sleep();
      }
      
  ```

  ```java
      
      // Implement the interface in a class
      class Dog implements Animal {
          @Override
          public void eat() {
              System.out.println("Dog eats");
          }
      
          @Override
          public void sleep() {
              System.out.println("Dog sleeps");
          }
      }
  
  ```

  ```java
      public class Main {
          public static void main(String[] args) {
              Animal dog = new Dog();
              dog.eat();
              dog.sleep();
          }
      }
  
  ```
  
  - An abstract class is a class that cannot be `instantiated` directly.
  - It can contain both `abstract methods` (methods without implementation) and `concrete methods` (methods with implementation).
  - An abstract class can have instance variables, constructors, and methods with or without implementation.
  - Subclasses must extend an abstract class and implement all its abstract methods, unless they are also declared abstract.
  - An abstract class can also provide default implementation for some methods, which subclasses may choose to override or not.
  - Cannot be declared `final`
  - Abstract methods should not be `private`
  - An `abstract class` can partially implement an `interface`
    
 ```java
     // Abstract class
    abstract class Vehicle {
        abstract void drive();
    
        void stop() {
            System.out.println("Vehicle stopped");
        }
    }

 ```
 ```java
    // Class implementing an interface and extending an abstract class
    class Car extends Vehicle implements Animal {
        @Override
        void drive() {
            System.out.println("Car is being driven");
        }
    
        @Override
        public void makeSound() {
            System.out.println("Car honks");
        }
    }
 ```
```java
    public class Main {
        public static void main(String[] args) {
            Car myCar = new Car();
            myCar.drive();
            myCar.makeSound();
            myCar.stop();
        }
    }
```

## Difference between Abstract Class and Interface

 ### Method Implementation:
 - Abstract Class: Can have both `abstract` and `concrete` methods.
 - Interface: Can only have `method signatures`, but from Java 8 onwards, can have `default` and `static` methods.
  
### Inheritance:
- Abstract Class: Supports both single inheritance and implementation inheritance. A Java class can extend only `one abstract class` due to `Java's single inheritance` model. It's possible to inherit fields and methods from an abstract class, and subclassing allows for code reuse and extension of functionality.
- Interface: Supports `multiple inheritance` through implementation. A Java class can `implement` multiple interfaces. Interfaces enable a form of multiple inheritance by allowing a class to declare that it implements multiple behaviors.
  
### Access Modifiers:
- Abstract Class: Can have constructors with various access modifiers `(public, protected, or package-private)`. Abstract classes can also have fields with any access modifier.
- Interface: All methods declared in an interface are by default `public` and `abstract`. Fields in interfaces are implicitly `public`, `static`, and `final`.
  
### Constructor:
- Abstract Class:  Can have constructors, which are called when a concrete subclass is instantiated. 
- Interface: Cannot have constructors because interfaces cannot be instantiated. They are meant to be implemented by classes, which provide the necessary constructors.

### Extension:
- Abstract Class: Extended using the `extends` keyword.
- Interface: Implemented using the `implements` keyword.
  
### Usage:
- Abstract Class: Used when you want to provide a common `base implementation` for a group of related classes. It's appropriate when you have a base class that contains some default behavior that subclasses can inherit and override.
- Interface: Used when you want to define a `contract` for a group of classes, specifying a `set of methods` that implementing classes must provide. Interfaces are useful for achieving `loose coupling` and allowing different classes to adhere to a common interface without being tightly coupled to each other.

## 7. Static
   - `Static Variable:` When a variable is declared as static within a class, it means that the variable belongs to the class itself rather than to any instance of the class. There will be only one copy of a static variable regardless of how many instances of the class are created. 

  ```java
      public class MyClass {
      public static int myStaticVariable = 10;
  
      public static void main(String[] args) {
          MyClass obj1 = new MyClass();
          MyClass obj2 = new MyClass();
  
          // Both objects share the same static variable
          obj1.myStaticVariable = 20;

          System.out.println("static variable: " + MyClass.myStaticVariable);  // 20
          System.out.println("obj1 static variable: " + obj1.myStaticVariable); // 20
          System.out.println("obj2 static variable: " + obj2.myStaticVariable);  // 20
      }
  }
```

  - `Static Method:`static method is a method that belongs to the class rather than to any specific instance of the class. This means you can call a static method without creating an instance of the class.
  - `No Access to Instance Variables `: Static methods cannot access instance variables directly because they don't belong to any instance. However, they can access static variables.
  - Cannot Use `this` Keyword Since static methods are not tied to any particular instance, they cannot use the this keyword to refer to the current instance.
  - Can Call other `static` methods directly.
    
  ```java
       public class MyClass {
      
            static void myStaticMethod() {
                System.out.println("This is a static method.");
            }
        
            public static void main(String[] args) {
                MyClass.myStaticMethod();
              }
            }
  ```
```java
public class MyClass {
    private static int count = 0; // Static variable

    public void incrementCount() {
        count++; // Accessing and modifying the static variable
    }

    public int getCount() {
        return count; // Accessing the static variable
    }
}
```
 ```java
      public class Main {  
      public static void main(String[] args) {
        MyClass.incrementCount();
        System.out.println(MyClass.getCount());
      }
  }
```
  - `Static Class:` In Java, classes themselves cannot be declared as static. They are loaded into memory when the program starts, and each instance of the class has its own memory. However, nested static classes are allowed. These nested classes belong to the outer class and can be instantiated without requiring an instance of the outer class.
    
 ```java
     public class OuterClass {
          static class NestedStaticClass {
              void display() {
                  System.out.println("This is a static nested class.");
              }
          }
      
          public static void main(String[] args) {
              OuterClass.NestedStaticClass nested = new OuterClass.NestedStaticClass();
              nested.display();
          }
     }
  ```

## 8. Final
- `Final Attribute (Variable):` A final attribute cannot be reassigned once initialized.
  
  ```java
    class MyClass {
        // Final attribute
        final int constant = 10;
    
        // Method attempting to change the value of constant
        public void changeValue() {
            // This would result in a compilation error
            // constant = 20;
        }
    }
    
    public class Main {
        public static void main(String[] args) {
            // Instantiate MyClass
            MyClass obj = new MyClass();
            // Access constant attribute
            System.out.println("Constant value: " + obj.constant);
        }
    }
  ```

- `Final Method:` A final method cannot be overridden in subclasses.
  
  ```java
      class Parent {
        // Final method
            public final void finalMethod() {
                // Method implementation
            }
        }
        
        public class Child extends Parent {
            // Attempting to override finalMethod will result in a compilation error
            // public void finalMethod() { }
            
            public static void main(String[] args) {
                // Instantiate Child class
                Child child = new Child();
                // Call finalMethod
                child.finalMethod();
            }
        }
  ```
- `Final Class:` When a class is declared as final, it means that it cannot be subclassed. This prevents other classes from inheriting from it.
  
   ```java
      final class FinalClass {
            // Class members and methods
        }
        
        public class Main {
            public static void main(String[] args) {
                // Instantiate FinalClass
                FinalClass obj = new FinalClass();
                // Access methods or members of FinalClass
            }
        }
   ```

   

# References
- [Java Guides](https://www.javaguides.net/)
- [GeeksforGeeks](https://www.geeksforgeeks.org/)

