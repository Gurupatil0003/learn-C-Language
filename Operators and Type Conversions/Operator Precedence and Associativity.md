# ⚙️ Operator Precedence and Associativity in C

## 📘 Introduction

In C programming, **operators** determine how operands are combined to produce a result.  
However, when an expression has **more than one operator**, the **order of evaluation** becomes important.

C follows two key concepts to control this order:

1. **Operator Precedence** — determines which operator is evaluated first.  
2. **Associativity** — determines the direction of evaluation (left to right or right to left) when operators have the same precedence.

Understanding these rules is crucial for writing **bug-free and predictable C programs**.

---

## 🧩 What is Operator Precedence?

**Operator Precedence** defines the **priority** of different operators in an expression.  
Operators with **higher precedence** are evaluated **before** those with lower precedence.

### Example:
```c
int x = 10 + 5 * 2;
```

## ✅ Explanation:
```c
* has higher precedence than +

So, 5 * 2 is evaluated first → 10

Then, 10 + 10 = 20

Hence, x = 20
```

## 🔁 What is Associativity?

When two or more operators have the same precedence, associativity decides which operator is evaluated first.

There are two types:

Type	Description	Example
1.Left-to-Right	Operators are evaluated from left to right	a - b + c
2.Right-to-Left	Operators are evaluated from right to left	a = b = c

# ⚙️ Operator Precedence and Associativity in C (Highest → Lowest)

## 📘 Introduction

In C, when multiple operators appear in a single expression, **operator precedence** determines **which operator is evaluated first**, and **associativity** determines **the direction** (left-to-right or right-to-left) in which operators of the same precedence are evaluated.

Understanding this helps you predict how complex expressions are executed.

---

## 🧠 Operator Precedence and Associativity Table

| Precedence (High → Low) | Category / Description | Operators | Associativity |
|--------------------------|------------------------|------------|----------------|
| **1** | **Postfix / Primary Operators** | `()` (Function Call), `[]` (Array Subscript), `->` (Structure Pointer), `.` (Structure Member), `++` (Post-Increment), `--` (Post-Decrement)` | **Left to Right** |
| **2** | **Unary Operators** | `+` (Unary Plus), `-` (Unary Minus), `++` (Pre-Increment), `--` (Pre-Decrement), `!` (Logical NOT), `~` (Bitwise NOT), `(type)` (Type Cast), `*` (Dereference), `&` (Address Of), `sizeof` | **Right to Left** |
| **3** | **Multiplicative Operators** | `*` (Multiplication), `/` (Division), `%` (Modulus) | **Left to Right** |
| **4** | **Additive Operators** | `+` (Addition), `-` (Subtraction) | **Left to Right** |
| **5** | **Shift Operators** | `<<` (Left Shift), `>>` (Right Shift) | **Left to Right** |
| **6** | **Relational Operators** | `<` (Less Than), `<=` (Less Than or Equal To), `>` (Greater Than), `>=` (Greater Than or Equal To) | **Left to Right** |
| **7** | **Equality Operators** | `==` (Equal To), `!=` (Not Equal To) | **Left to Right** |
| **8** | **Bitwise AND** | `&` | **Left to Right** |
| **9** | **Bitwise XOR** | `^` | **Left to Right** |
| **10** | **Bitwise OR** | `\|` | **Left to Right** |
| **11** | **Logical AND** | `&&` | **Left to Right** |
| **12** | **Logical OR** | `\|\|` | **Left to Right** |
| **13** | **Conditional / Ternary Operator** | `?:` | **Right to Left** |
| **14** | **Assignment Operators** | `=`, `+=`, `-=`, `*=`, `/=`, `%=` , `<<=`, `>>=`, `&=`, `^=`, `\|=` | **Right to Left** |
| **15** | **Comma Operator** | `,` | **Left to Right** |

---


