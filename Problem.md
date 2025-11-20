# Ticket ID Generator – Static Variable Simulation

This project simulates a helpdesk system that generates **sequential, unique ticket IDs** during a program run. It demonstrates the use of a **static local variable** inside a function to maintain state across multiple calls.

---

## 📘 Problem Statement

A helpdesk system generates ticket IDs in sequence.  
Implement a function `next_id()` that:

- Uses a **static local variable** to persist its value between calls.
- Returns `1` on the first call, `2` on the second, and so on.

Given an integer `n`, call this function `n` times and output all generated IDs.

---

## 📥 Input Format

- A single integer `n` (≥ 0)  
  Represents how many ticket IDs to generate.

---

## 📤 Output Format

- A single line containing `n` ticket IDs separated by spaces.
- IDs begin at `1` and increment by `1` each call.
- If `n = 0`, output nothing.

---

## 🧪 Sample Test Cases

### ✔️ Sample Test Case 1

**Input**
```c
5
```

**Output**

```c
1 2 3 4 5
```

### ✔️ Sample Test Case 2

**Input**

```c
1
```

**Output**

```c
1
```

# Email Privacy Masking – In-Place Pointer Manipulation

This project implements an email privacy filter that **masks the username portion** of an email address.  
Only the **first** and **last** characters of the username are kept, while all characters in between are replaced with asterisks (`*`).  
The username (portion before `@`) is also converted to **lowercase**, using `<ctype.h>`.  
The domain (portion after `@`) remains unchanged.

---

## 📘 Problem Statement

Define a function that:

- Modifies the email **in place** using **pointers**.
- Converts the **username only** to lowercase.
- Replaces all characters between the first and last username characters with `*`.
- Leaves the domain unchanged.

---

## 📥 Input Format

- A single email string (no spaces).

---

## 📤 Output Format

- The masked email, following the privacy rules.

---

## 🧪 Sample Test Cases

### ✔️ Sample Test Case 1

**Input**
```c
Alice.Wonder@Example.com
```

**Output**

```c
a**********r@Example.com
```

**Explanation:**  

Username `Alice.Wonder` → lowercased to `alice.wonder` → masked to `a**********r`.

---

### ✔️ Sample Test Case 2

**Input**

```c
X@site.io
```

**Output**

```c
x@site.io
```

# Product Key Validator – Pattern Checking with `<ctype.h>`

This project validates product keys printed by a production line.  
A correct product key follows the format: **AB12-CD34** — exactly 9 characters long, with a hyphen at position 5, and all other characters alphanumeric.

---

## 📘 Problem Statement

A production line prints product keys like `AB12-CD34`.  
Define a function that checks if a key is valid:

- Must be **exactly 9 characters**
- Character at position **5** (index 4) must be a hyphen `-`
- All other characters must be **alphanumeric**  
- Use `<ctype.h>` to validate characters

Print `Valid` or `Invalid`.

---

## 📥 Input Format

- One product key (no spaces)

---

## 📤 Output Format

- `Valid` or `Invalid`

---

## 🧪 Sample Test Cases

### ✔️ Sample Test Case 1

**Input**
```c
AB12-CD34
```

**Output**

```c
Valid
```

**Explanation:**  
Matches pattern.

---

### ✔️ Sample Test Case 2

**Input**

```c
-a1b2c-d3e4
```

**Output**

```c
Invalid
```

# KPI Summary Generator – Min, Max, and Average Functions

This project computes a quick KPI summary from **n daily metric values**.  
To support clean and modular code, the program implements three **separate, non-recursive** functions:

- `min_val` – returns the smallest value  
- `max_val` – returns the largest value  
- `avg_val` – returns the average of all values  

The program reads `n` integers and outputs the minimum, maximum, and average (rounded to two decimal places).

---

## 📘 Problem Statement

An operations dashboard generates a quick KPI summary from n daily metric values.  
To support modular and maintainable code, implement three separate, non-recursive functions:

- `min_val` to find the smallest value  
- `max_val` to find the largest value  
- `avg_val` to compute the average  

Read n integers, then output the minimum, maximum, and average (rounded to two decimal places) on a single line.

---

## 📥 Input Format

- The first integer is **n** (number of metrics, n ≥ 1)  
- Followed by **n integers** representing the daily metric values  
- All values appear on one line, separated by spaces

---

## 📤 Output Format

One line containing three values separated by spaces:

1. The minimum (integer)  
2. The maximum (integer)  
3. The average (formatted to **two decimal places**)  

---

## 🧪 Sample Test Cases

### ✔️ Sample Test Case 1

**Input**
```c
5
10 20 30 40 50
```

**Output**

```c
10 50 30.00
```

**Explanation:**  
```c
Min = 10, Max = 50, Avg = 30.00

```

### ✔️ Sample Test Case 2

**Input**

```c
4
-1 -1 -1 -1

```
**Output**

```c
-1 -1 -1.00
```

# Case-Insensitive Username Comparison – Using `<ctype.h>`

This project implements a user-defined function that compares two usernames **ignoring letter case**.  
Both strings are compared lexicographically after converting characters to the same case (lower or upper) using `<ctype.h>`.  
The function returns:

- `-1` if `u < v`  
- `0` if equal  
- `1` if `u > v`  

The program prints the comparison result.

---

## 📘 Problem Statement

During login, two usernames should be considered equal ignoring letter case.  
Write a user-defined function that compares two strings case-insensitively using `<ctype.h>` (convert both to lower or upper while comparing) and returns -1, 0, or 1. Print the result.

---

## 📥 Input Format

Two strings `u` & `v` (no spaces)

---

## 📤 Output Format

-1 if u < v,
0 if equal,
1 if u > v (case-insensitive)


---

## 🧪 Sample Test Cases

### ✔️ Sample Test Case 1

**Input**

```c
Alice alice
```

**Output**

```c
0
```

**Explanation:**  
Same ignoring case.

---

### ✔️ Sample Test Case 2

**Input**

```c
beta Alpha
```

**Output**
```c

1
```

# Temperature Conversion – Celsius ↔ Fahrenheit Using Functions

This project implements two user-defined functions to convert temperature values between Celsius and Fahrenheit.  
The program clearly demonstrates **function declaration, definition, and invocation**, then prints the converted value rounded to **two decimal places**.

---

## 📘 Problem Statement

An IoT gateway receives a reading and a unit code.  
Create two user-defined functions: `c_to_f` and `f_to_c`.  
If unit is `C`, convert Celsius to Fahrenheit; if `F`, convert Fahrenheit to Celsius.  
Show function declaration, definition, and invocation clearly, and print the converted value to two decimals.

---

## 📥 Input Format

`value unit`  
(where unit is `C` or `F`)

---

## 📤 Output Format

- Converted value, formatted to **two decimal places**

---

## 🧪 Sample Test Cases

### ✔️ Sample Test Case 1

**Input**
**Input**

```c
0 C
```

**Output**
```c
32.00

```
**Explanation:**
```c
0°C → 32°F.
```

### ✔️ Sample Test Case 2

**Input**
```c
212 F
```

**Output**
```c
100.00
```

**Explanation:**  
```c
212°F → 100°C.
```
