# 🐍 Python Cheat Sheet for Humans Who Need to Get Stuff Done

A high-speed guide to learning Python that skips the theory BS and jumps straight into **what you actually need** to write clean, functional code for real-world projects.

---

## 1️⃣ Python Basics

### 🔤 Variables

```python
language = "Python"
version = 3.10
is_fun = True
```

🔢 Data Types

- int-whole number(42)
- float-decimal(3.14)
- str-string("cheat sheet")
- bool-True or False
- list-ordered collection[1, 2, 3]
- dict-key value pair:{"language": "Python", "level":  "Beginner"}

---

### 🤔 `if` Statements

Use `if`, `elif`, and `else` to make decisions based on conditions.

```python
temperature = 75

if temperature > 85:
    print("Too hot!")
elif temperature < 60:
    print("Too cold!")
else:
    print("Just right.")
```

You can use logical operators too:

```python
age = 20

if age >= 18 and age < 65:
    print("You're an adult.")
```

---

🛠️ Defining and Using Functions

Functions let you group code into reusable tools.

```python
def greet_user(name):
    print(f"Hello, {name}!")
    
greet_user("Ada")
```

Return values from a function like this:

```python
def square(x):
    return x * x

result = square(5)
print(result)  # 25
```

Functions help you:

- Write once, use many times
- Test small parts of code
- Keep logic organized

---

## 3️⃣ Collections: Lists, Tuples, and Dictionaries

### 📋 `list`: A flexible, ordered group of items

```python
fruits = ["apple", "banana", "cherry"]
print(fruits[0])      # "apple"
fruits.append("kiwi") # add item
print(len(fruits))    # 4
```

Lists are mutable (you can change them).

---

## 🧊 tuple: An unchangeable list (immutable)

dimensions = (10, 20, 30)
print(dimensions[1])  # 20

---

## 🧠 dict: A key-value data structure

```python
person = {"name": "Alice", "age": 30}
print(person["name"])     # "Alice"
person["age"] += 1        # now 31
```

Dictionaries are your best friend when working with:
- Data rows
- Configs
- Anything with labels + values

---

## 🔁 Looping through them

```python
# Loop through list
for fruit in fruits:
    print(fruit)

# Loop through dict
for key, value in person.items():
    print(f"{key}: {value}")
```

---

### 💡 When to Use What?

| Type     | Ordered? | Mutable? | Use Case                            |
|----------|----------|----------|-------------------------------------|
| `list`   | ✅        | ✅        | General-purpose sequences           |
| `tuple`  | ✅        | ❌        | Coordinates, constants              |
| `dict`   | ❌        | ✅        | Keyed data, configurations, records |

---

## 4️⃣ Intro to `pandas`: Python for Data Work

`pandas` is the most popular library for working with **structured data** in Python. Think spreadsheets, CSVs, tables—anything with rows and columns.

---

### 🧠 First, import it:

```python
import pandas as pd
```

---

📥 Reading Data

```python
df = pd.read_csv("data.csv")  # Load a CSV file
```

You can view it:

```python
df.head()     # First 5 rows
df.tail(3)    # Last 3 rows
df.shape      # (rows, columns)
```

---

🧼 Cleaning & Prepping

```python
df.columns = df.columns.str.strip()     # Remove whitespace in headers
df.dropna(how="all", inplace=True)      # Drop empty rows
df = df.drop_duplicates()               # Remove duplicates
```

---

🔍 Accessing Data

```python
df["ColumnName"]        # Single column
df[["A", "B", "C"]]     # Multiple columns

df.loc[0]               # First row (by label)
df.iloc[0]              # First row (by index)
```

---

📏 Filtering Rows
```python
df[df["Age"] > 30]             # Rows where Age > 30
df[df["Status"] == "Active"]   # Filter by string match
```

---

🧮 Adding & Modifying Columns

```python
df["Total"] = df["Price"] * df["Quantity"]  # New column from math
df["Active"] = True                         # Add constant column
```

---

📊 Descriptive Statistics

```python
df.describe()         # Summary of numeric columns
df["Score"].mean()    # Average of one column
df["Score"].value_counts()  # Frequency table
```

---

💡 Why pandas?

✅ Fast and flexible
✅ Works great with .csv, .xlsx, SQL, APIs
✅ 10x easier to clean data than Excel
✅ Used in literally every data science job


---

### 🥊 `pandas` vs Excel: Why Python Wins at Data Work

| Feature                    | Excel                           | `pandas`                           |
|----------------------------|----------------------------------|------------------------------------|
| 📈 Data size               | Struggles above ~50,000 rows     | Easily handles millions of rows    |
| ⏱️ Speed                  | Manual clicks, slow recalcs      | Fast, automated operations         |
| 🔄 Reproducibility         | “Hope you saved it right”        | Scripted, repeatable workflows     |
| 💡 Logic & filters         | Built-in formulas (VLOOKUP, etc) | Custom logic with full Python power|
| 🧼 Cleaning messy data     | Tedious and manual               | One-liner `.dropna()`, `.fillna()` |
| 🧪 Testing                 | LOL                             | Unit tests and assert statements   |
| 🧠 Scalability             | 😬                              | 😎                                 |
| 💻 Automation              | VBA (🤮)                         | Full Python scripting              |
| 📝 Version control         | “Final_Final_V2_REAL.xlsx”       | Git + code = sanity                |

---

> **Verdict**: Use Excel when you're doing a quick summary.  
> Use `pandas` when you’re doing *literally anything that matters.*

---

## 5️⃣ Advanced Loops: List Comprehensions & `.apply()`

### 🔁 List Comprehensions

Cleaner, faster way to create lists from loops.

```python
# Traditional loop
squares = []
for x in range(5):
    squares.append(x**2)

# List comprehension
squares = [x**2 for x in range(5)]
```

Use with conditions:

```python
even = [x for x in range(10) if x % 2 == 0]
```

---

🧠 .apply() in pandas

```python
# Apply a built-in function
df["ScoreRounded"] = df["Score"].apply(round)

# Apply your own function
def pass_fail(x):
    return "Pass" if x >= 60 else "Fail"

df["Result"] = df["Score"].apply(pass_fail)
```

.apply() = way better than looping through DataFrame rows manually.

---

💡 Use list comprehensions for small, fast list creation.
Use .apply() for data cleaning, column transformations, and logic.

---