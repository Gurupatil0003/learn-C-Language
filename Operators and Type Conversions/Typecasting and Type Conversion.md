## 🔹 Typecasting and Type Conversion

**Typecasting** and **Type Conversion** are methods used to convert the data type of a variable into another data type.

---

### 🧠 1. Type Conversion (Implicit Conversion)

Also known as **implicit type casting** or **coercion**.  
It is automatically performed by **Python** when data types are compatible — the conversion happens **without user intervention**.

#### 🧩 Example:
```python
x = 10      # int
y = 3.5     # float

result = x + y   # int is automatically converted to float
print(result)    # Output: 13.5
print(type(result))  # <class 'float'>
```
## ✅ Explanation:
Python converts x (int) to float before addition to avoid data loss.

## 🧠 2. Typecasting (Explicit Conversion)

Also known as explicit type conversion.
Here, the user manually converts one data type to another using built-in functions.

🧩 Example:
```c
a = "100"
b = int(a)    # Converts string to integer
print(b + 50) # Output: 150
```
