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
