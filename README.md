<div dir="ltr" align="left">

# C++ Beginner Tutorial — Single Session (Up to Arrays)
> This file is designed to teach basic C++ concepts to beginners. It contains detailed explanations and simple examples so you can cover all foundational topics in one session. **Functions, arrays, strings, and vectors** are excluded in this version.

---

## 🎯 Learning Objectives
- Understand the general structure of a C++ program and how it executes.
- Learn to define variables and basic data types.
- Understand operators, especially increment and decrement operators.
- Get familiar with conditionals (`if`, `else`, `switch`) and loops (`for`, `while`, `do-while`).

---

## 🧩 1) Introduction and Basic Structure
C++ is a powerful and widely used programming language in fields like engineering, simulation, and game development. Every C++ program starts from the `main()` function and usually contains statements for input and output.

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello World!" << endl;
    return 0;
}
```

**Explanation:**
- `#include <iostream>` allows using input and output commands.
- `using namespace std;` removes the need to write `std::` before `cout` or `cin`.
- `main()` is the starting point of the program.
- `return 0;` indicates successful execution.

---

## 💬 2) Input and Output
In C++, `cout` is used for output, and `cin` for input.

```cpp
#include <iostream>
using namespace std;

int main() {
    string name;
    int age;
    cout << "Enter your name: ";
    cin >> name;
    cout << "Enter your age: ";
    cin >> age;
    cout << "Hello " << name << ", you are " << age << " years old." << endl;
    return 0;
}
```

> Note: `cout` stands for console output and `cin` stands for console input.

---

## 🧠 3) Data Types and Variable Declaration
In C++, **variables** store data and must have a specific data type.

| Data Type | Description | Example |
|-----------|-------------|--------|
| `int` | Integer | `int x = 10;` |
| `double` | Decimal number | `double pi = 3.14;` |
| `char` | Single character | `char grade = 'A';` |
| `bool` | True or false | `bool isOk = true;` |
| `string` | Text (word or sentence) | `string name = "Ali";` |

**Important Notes:**
- Variable names cannot start with a number.
- Case-sensitive (`Age` and `age` are different).
- Multiple variables of the same type can be declared together:
  ```cpp
  int a = 10, b = 20, c = 30;
  ```

**Example:**
```cpp
int number = 5;
double price = 12.5;
char letter = 'C';
bool passed = false;
```

---

## ➕ 4) Operators
### a) Arithmetic Operators
| Operator | Meaning | Example |
|----------|---------|--------|
| `+` | Addition | `x + y` |
| `-` | Subtraction | `x - y` |
| `*` | Multiplication | `x * y` |
| `/` | Division | `x / y` |
| `%` | Modulus | `x % y` |

### b) Comparison Operators
| Operator | Meaning | Example |
|----------|---------|--------|
| `==` | Equal to | `x == y` |
| `!=` | Not equal | `x != y` |
| `>` | Greater than | `x > y` |
| `<` | Less than | `x < y` |
| `>=` | Greater or equal | `x >= y` |
| `<=` | Less or equal | `x <= y` |

### c) Logical Operators
| Operator | Meaning | Example |
|----------|---------|--------|
| `&&` | AND | `(x > 0 && y > 0)` |
| `\|\|` | OR | `(x > 0 \|\| y > 0)` |
| `!` | NOT | `!(x > 0)` |

---

## 🔁 5) Increment and Decrement Operators (++ and --)
These operators are used to increase or decrease a variable.

```cpp
int i = 5;
i++; // i = 6
++i; // i = 7
```

Prefix (`++i`) vs. Postfix (`i++`):
- `++i`: increases first, then uses the value.
- `i++`: uses the value first, then increases.

Example:
```cpp
int a = 5;
cout << a++ << endl; // prints 5, then a becomes 6
cout << ++a << endl; // a becomes 7, then prints 7
```

Similarly:
```cpp
int b = 5;
b--; // b = 4
--b; // b = 3
```

---

## ⚙️ 6) Conditionals (if / else / switch)
Conditionals are used to make decisions in programs.

```cpp
int number;
cout << "Enter a number: ";
cin >> number;

if (number > 0) {
    cout << "Positive number" << endl;
} else if (number < 0) {
    cout << "Negative number" << endl;
} else {
    cout << "Zero" << endl;
}
```

---

## 🔄 7) Loops
Loops execute a block of code multiple times. C++ has three main loop types:

### 🔹 `for` loop
Used when the number of iterations is known.
```cpp
for (int i = 1; i <= 5; i++) {
    cout << i << " ";
}
```

### 🔹 `while` loop
Used when the number of iterations is unknown and the loop continues as long as a condition is true.
```cpp
int i = 1;
while (i <= 5) {
    cout << i << " ";
    i++;
}
```

### 🔹 `do-while` loop
Similar to `while`, but **executes at least once even if the condition is false**.
```cpp
int i = 1;
do {
    cout << i << " ";
    i++;
} while (i <= 5);
```

### 🔹 `break` and `continue`
- `break`: exits the loop immediately.
- `continue`: skips to the next iteration without executing the remaining statements in the loop.

Example:
```cpp
for (int i = 1; i <= 5; i++) {
    if (i == 3) continue; // skip printing 3
    if (i == 5) break;    // exit loop when i is 5
    cout << i << " ";
}
// output: 1 2 4
```

---

## 🧭 8) `switch-case` Statement
Used when you want to check multiple possible values of a variable (instead of multiple `if-else`).

```cpp
int day = 3;
switch (day) {
    case 1:
        cout << "Saturday";
        break;
    case 2:
        cout << "Sunday";
        break;
    case 3:
        cout << "Monday";
        break;
    case 4:
        cout << "Tuesday";
        break;
    case 5:
        cout << "Wednesday";
        break;
    default:
        cout << "Invalid day";
}
```

---

## 📚 Useful Resources
- [W3Schools C++ Tutorial](https://www.w3schools.com/cpp/)
- cppreference.com for