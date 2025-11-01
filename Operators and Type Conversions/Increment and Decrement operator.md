# Increment and Decrement Operators in C

## 🧠 Introduction

In C, **increment** and **decrement** operators are **unary operators** (they work on a single operand).  
They are used to **increase or decrease** the value of a variable by `1`.

These operators are very common in **loops**, **counters**, and **expressions**.

---

## ⚙️ Types of Operators

### 1. Increment Operator (`++`)
Increases the value of a variable by `1`.

### 2. Decrement Operator (`--`)
Decreases the value of a variable by `1`.

---

## 🔄 Forms of Increment/Decrement Operators

Both operators have **two forms**:

| Type | Example | Description |
|------|----------|-------------|
| **Pre-increment** | `++x` | Increments `x` first, then uses the updated value. |
| **Post-increment** | `x++` | Uses the current value of `x` first, then increments it. |
| **Pre-decrement** | `--x` | Decrements `x` first, then uses the updated value. |
| **Post-decrement** | `x--` | Uses the current value first, then decrements it. |

# 🧩 Example 1 — Increment and Decrement (Basic Demonstration)

**Example Code**

```c
#include <stdio.h>

int main() {
    int a = 5;

    printf("Initial value of a: %d\n", a);

    a++; // post-increment
    printf("After a++ : %d\n", a);

    ++a; // pre-increment
    printf("After ++a : %d\n", a);

    a--; // post-decrement
    printf("After a-- : %d\n", a);

    --a; // pre-decrement
    printf("After --a : %d\n", a);

    return 0;
}
```
Output:

```c

Initial value of a: 5
After a++ : 6
After ++a : 7
After a-- : 6
After --a : 5
```

## 🧠 Example 2 — Difference Between Pre and Post Increment

**Example Code**

```c
#include <stdio.h>

int main() {
    int x = 10, y;

    y = ++x; // Pre-increment: x becomes 11, then y = 11
    printf("Pre-increment: x = %d, y = %d\n", x, y);

    x = 10;
    y = x++; // Post-increment: y = 10, then x becomes 11
    printf("Post-increment: x = %d, y = %d\n", x, y);

    return 0;
}
```

## Output:

```c
Pre-increment: x = 11, y = 11
Post-increment: x = 11, y = 10
```
**Explanation:**

- In **pre-increment**, the variable is increased **before** it’s used.  
- In **post-increment**, the variable is increased **after** it’s used.  
- The same logic applies to **decrement (`--`)** operators.

---

## 🔁 Example 3 — Using in Expressions

**Example Code**

```c
#include <stdio.h>

int main() {
    int a = 5, b = 10, result;

    result = a++ + ++b; // a++ (use 5, then a=6), ++b (b=11, use 11)
    printf("Result = %d\n", result);
    printf("a = %d, b = %d\n", a, b);

    return 0;
}
Output:

```c
Result = 16
a = 6, b = 11
```
### Step-by-step Explanation:
```c
a++ → uses 5, then a becomes 6.

++b → increments b to 11 and uses 11.

Therefore, Result = 5 + 11 = 16.
```

## 🧮 Example 4 — Using in Loops

Increment and decrement operators are commonly used in **`for`**, **`while`**, and **`do-while`** loops to control iteration.

---

**Example Code**

```c
#include <stdio.h>

int main() {
    int i;

    printf("Counting up using ++:\n");
    for (i = 1; i <= 5; i++) {
        printf("%d ", i);
    }

    printf("\nCounting down using --:\n");
    for (i = 5; i >= 1; i--) {
        printf("%d ", i);
    }

    return 0;
}
```
## Output:

```c
Counting up using ++:
1 2 3 4 5 
Counting down using --:
5 4 3 2 1
```
