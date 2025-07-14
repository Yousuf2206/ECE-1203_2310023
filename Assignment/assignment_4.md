## Assignment No: 04
## Assignment Name: Usage of C++ Keywords with Example
## Submission Date: 14 July, 2025

---

### Keyword 01: `asm`

**Use:**  
Embeds low-level assembly code directly into C++. Useful for system programming, performance tuning, or accessing hardware-level instructions.

**Example:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10, b = 20, result;
    asm("addl %%ebx, %%eax;" : "=a"(result) : "a"(a), "b"(b));
    cout << result;
    return 0;
}
```

---

### Keyword 02: `auto`

**Use:**  
Automatically deduces the type of a variable from its initializer. It helps make code cleaner and more flexible.

**Example:**
```cpp
auto a = 42;       // int
auto b = 3.14;     // double
auto message = "Hello"; // const char*

auto multiply(int x, double y) {
    return x * y;
}
```

---

### Keyword 03: `bool`

**Use:**  
Represents a boolean value — `true` or `false`. Commonly used for conditions.

**Example:**
```cpp
bool active = true;
bool check = (5 > 3);
cout << active << " " << check;
```

---

### Keyword 04: `break`

**Use:**  
Exits a loop or switch block prematurely when a condition is met.

**Example:**
```cpp
for (int i = 0; i < 10; i++) {
    if (i == 5) break;
    cout << i << " ";
}

int choice = 2;
switch (choice) {
    case 1: cout << "One"; break;
    case 2: cout << "Two"; break;
}
```

---

### Keyword 05: `case`

**Use:**  
Defines a specific branch inside a switch statement.

**Example:**
```cpp
int day = 2;
switch (day) {
    case 1: cout << "Monday"; break;
    case 2: cout << "Tuesday"; break;
    default: cout << "Other day";
}
```

---

### Keyword 06: `catch`

**Use:**  
Handles exceptions thrown in a try block. Ensures graceful error handling.

**Example:**
```cpp
try {
    throw runtime_error("Something went wrong");
} catch (const exception& e) {
    cout << "Error: " << e.what();
}
```

---

### Keyword 07: `char`

**Use:**  
Stores a single character, typically using ASCII encoding.

**Example:**
```cpp
char letter = 'A';
cout << letter;
```

---

### Keyword 08: `class`

**Use:**  
Defines a blueprint for creating objects, combining data and functions.

**Example:**
```cpp
class Rectangle {
public:
    double width, height;

    double area() {
        return width * height;
    }
};
```

---

### Keyword 09: `const`

**Use:**  
Makes a variable or pointer read-only after initialization.

**Example:**
```cpp
const int size = 100;
int value = 10;

const int* p1 = &value;
int* const p2 = &value;
const int* const p3 = &value;
```

---

### Keyword 10: `const_cast`

**Use:**  
Safely adds or removes `const` from a variable type.

**Example:**
```cpp
int x = 5;
const int* ptr = &x;
int* modifiable = const_cast<int*>(ptr);
*modifiable = 10;
cout << x;
```
