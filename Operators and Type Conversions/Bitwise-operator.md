# 🧠 Bitwise Operators in C

## 📘 Introduction

Bitwise operators in C are used to **perform operations on individual bits** of integer data types such as `int`, `char`, or `long`.  
They are **faster** and often used in **embedded systems, device drivers, and performance-critical applications**.

Each bit of the operands is compared and manipulated **bit by bit**.

---

## 🧩 Types of Bitwise Operators

| Operator | Symbol | Operation Name | Description |
|-----------|---------|----------------|--------------|
| AND | `&` | Bitwise AND | Sets each bit to 1 if **both** bits are 1 |
| OR | `|` | Bitwise OR | Sets each bit to 1 if **any** bit is 1 |
| XOR | `^` | Bitwise XOR (Exclusive OR) | Sets each bit to 1 if **only one** bit is 1 |
| NOT / Complement | `~` | Bitwise Complement | Inverts all bits (1 → 0, 0 → 1) |
| Left Shift | `<<` | Shift Left | Shifts bits to the left by given positions |
| Right Shift | `>>` | Shift Right | Shifts bits to the right by given positions |

---


## 🔹 1. Bitwise AND (`&`)

**Rule:**
```c
1 & 1 → 1
Otherwise → 0
```


**Example:**
```c
#include <stdio.h>
int main() {
    int a = 5, b = 3;     // 5 = 0101, 3 = 0011
    int result = a & b;   // 0101 & 0011 = 0001
    printf("a & b = %d\n", result);  // Output: 1
    return 0;
}
```
## Explanation:
```
  0101 (5)
& 0011 (3)
  ----
  0001 → 1

```

##🔹 2. Bitwise OR (|)

**Rule:**
```c
1 | 1 → 1  
1 | 0 → 1  
0 | 0 → 0
```

## Example:
```c
int a = 5, b = 3;
printf("a | b = %d\n", a | b); // Output: 7
```

## Explanation:
```
  0101 (5)
| 0011 (3)
  ----
  0111 → 7
```
## 🔹 3. Bitwise XOR (^)

**Rule:**
```c
1 ^ 1 → 0  
0 ^ 0 → 0  
1 ^ 0 → 1  
0 ^ 1 → 1
```

## Example:
```
int a = 5, b = 3;
printf("a ^ b = %d\n", a ^ b); // Output: 6
```

## Explanation:

```c
  0101 (5)
^ 0011 (3)
  ----
  0110 → 6
```

##🔹 4. Bitwise Complement (~)

**Rule:**
## Each bit is flipped:
```c
1 → 0  
0 → 1
```

## Example:
```c
int a = 5;
printf("~a = %d\n", ~a);
```

## Explanation:
```c
a = 0000 0101
~a = 1111 1010 → In decimal: -6
```

##🔹 5. Left Shift (<<)

- Shifts bits to the left and fills with 0s on the right.

## Example:
```c
int a = 5; // 0000 0101
printf("a << 1 = %d\n", a << 1);
printf("a << 2 = %d\n", a << 2);
```

## Explanation:
```
a << 1 : 0000 1010 → 10
a << 2 : 0001 0100 → 20
```

## Rule:
```c
a << n = a × (2ⁿ)
```

## 🔹 6. Right Shift (>>)

- Shifts bits to the right and discards bits on the right.

## Example:
```c
int a = 20; // 0001 0100
printf("a >> 1 = %d\n", a >> 1);
printf("a >> 2 = %d\n", a >> 2);
```

## Explanation:
```c
a >> 1 : 0000 1010 → 10
a >> 2 : 0000 0101 → 5
```

### Rule:
```c
a >> n = a ÷ (2ⁿ)
```
