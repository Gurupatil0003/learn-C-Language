# Introduction to Operators in C

In C, an **operator** is a symbol that tells the compiler to perform a specific operation on one or more **operands** (variables or values).

- **Operands:** The values or variables on which the operation is performed.  
- **Operators:** Symbols that perform actions like arithmetic, comparison, logical checks, or assignment.

C operators are classified into different types based on their functionality:

## 1. Arithmetic Operators
Used for performing mathematical calculations:  
`+`, `-`, `*`, `/`, `%`

## 2. Relational Operators
Used for comparing values:  
`==`, `!=`, `>`, `<`, `>=`, `<=`

## 3. Logical Operators
Used for combining logical conditions:  
`&&`, `||`, `!`

## 4. Assignment Operators
Used for assigning or updating values:  
`=`, `+=`, `-=`, `*=`, `/=`, `%=`

## 5. Other Operators
- Increment/decrement: `++`, `--`  
- Bitwise: `&`, `|`, `^`, `~`, `<<`, `>>`  
- Conditional: `?:`  
- Etc.


<img width="1024" height="1536" alt="image" src="https://github.com/user-attachments/assets/bd9da9de-28e1-4236-815e-9a8465f40a78" />

# Operators in C

## 1. Arithmetic Operators

Used for mathematical operations.

| Operator | Description      | Example |
|----------|-----------------|---------|
| `+`      | Addition        | `a + b` |
| `-`      | Subtraction     | `a - b` |
| `*`      | Multiplication  | `a * b` |
| `/`      | Division        | `a / b` |
| `%`      | Modulus (remainder) | `a % b` |

**Example Code**

```c
#include <stdio.h>

int main() {
    int a = 15, b = 4;

    printf("a + b = %d\n", a + b); // 19
    printf("a - b = %d\n", a - b); // 11
    printf("a * b = %d\n", a * b); // 60
    printf("a / b = %d\n", a / b); // 3
    printf("a %% b = %d\n", a % b); // 3

    return 0;
}
```

## 2. Relational (Comparison) Operators

Used to compare values. Return `1` (true) or `0` (false).

| Operator | Description                     |
|----------|---------------------------------|
| `==`     | Equal to                        |
| `!=`     | Not equal to                    |
| `>`      | Greater than                    |
| `<`      | Less than                       |
| `>=`     | Greater than or equal to        |
| `<=`     | Less than or equal to           |

**Example Code**

```c
#include <stdio.h>

int main() {
    int x = 10, y = 20;

    printf("x == y: %d\n", x == y); // 0
    printf("x != y: %d\n", x != y); // 1
    printf("x > y: %d\n", x > y);   // 0
    printf("x < y: %d\n", x < y);   // 1
    printf("x >= y: %d\n", x >= y); // 0
    printf("x <= y: %d\n", x <= y); // 1

    return 0;
}
```

Notes:
Relational operators are often used in if, while, and for statements.

## 3. Logical Operators

Used to combine or invert boolean expressions.

| Operator | Description                           |
|----------|---------------------------------------|
| `&&`     | Logical AND: true if both operands true |
| `||`     | Logical OR: true if at least one operand true |
| `!`      | Logical NOT: inverts value            |

**Example Code**

```c
#include <stdio.h>

int main() {
    int a = 1, b = 0;

    printf("a && b = %d\n", a && b); // 0
    printf("a || b = %d\n", a || b); // 1
    printf("!a = %d\n", !a);         // 0
    printf("!b = %d\n", !b);         // 1

    return 0;
}
```

Notes:

Logical operators return 1 (true) or 0 (false).

Often used in decision-making and loops.

## 4. Assignment Operators

Used to assign or update values of variables.

| Operator | Meaning                                |
|----------|----------------------------------------|
| `=`      | Assign value                            |
| `+=`     | Add and assign (`x += 3` → `x = x + 3`) |
| `-=`     | Subtract and assign                     |
| `*=`     | Multiply and assign                     |
| `/=`     | Divide and assign                       |
| `%=`     | Modulus and assign                      |

**Example Code**

```c
#include <stdio.h>

int main() {
    int x = 10;

    x += 5; // x = 15
    printf("x += 5: %d\n", x);

    x -= 3; // x = 12
    printf("x -= 3: %d\n", x);

    x *= 2; // x = 24
    printf("x *= 2: %d\n", x);

    x /= 4; // x = 6
    printf("x /= 4: %d\n", x);

    x %= 5; // x = 1
    printf("x %%= 5: %d\n", x);

    return 0;
}
```

## 5. Combined Example: All Operators in One Program

**Example Code**

```c
#include <stdio.h>

int main() {
    int a = 10, b = 3;
    int sum, diff, prod, div, mod;
    int x = 5, y = 10;
    int result;

    // Arithmetic Operators
    sum = a + b;
    diff = a - b;
    prod = a * b;
    div = a / b;
    mod = a % b;
    printf("Arithmetic: %d %d %d %d %d\n", sum, diff, prod, div, mod);

    // Relational Operators
    printf("Relational: %d %d %d %d %d %d\n", 
           a == b, a != b, a > b, a < b, a >= b, a <= b);

    // Logical Operators
    printf("Logical: %d %d %d\n", (x > 0 && y > 0), (x > 0 || y < 0), !(x > y));

    // Assignment Operators
    x = 5;
    x += 2; // 7
    x *= 3; // 21
    x -= 1; // 20
    printf("Assignment: %d\n", x);

    return 0;
}
Output:
```
```c
Arithmetic: 13 7 30 3 1
Relational: 0 1 0 1 0 1
Logical: 1 1 1
Assignment: 20
```
