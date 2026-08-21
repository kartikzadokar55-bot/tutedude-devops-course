# 🐍 Python Variables & Data Types

## 1. Variables

A variable is a name used to store a value in memory.

Example:

```python
name = "Kartik"
age = 23
experience = 2
```

Python does not require us to explicitly declare the variable's data type.

```python
name = "Kartik"
age = 23
```

---

## 2. Rules for Naming Variables

Valid:

```python
name = "Kartik"
age = 23
user_name = "admin"
```

Invalid:

```python
2name = "Kartik"
user-name = "Kartik"
```

### Rules

- Must start with a letter or `_`
- Cannot start with a number
- Cannot contain spaces
- Cannot use Python keywords
- Variable names are case-sensitive

Example:

```python
name = "Kartik"
Name = "Rahul"
```

`name` and `Name` are different variables.

---

# 3. Python Data Types

Python has several built-in data types.

| Data Type | Example |
|---|---|
| `str` | `"Kartik"` |
| `int` | `23` |
| `float` | `3.14` |
| `bool` | `True` |
| `list` | `[1, 2, 3]` |
| `tuple` | `(1, 2, 3)` |
| `set` | `{1, 2, 3}` |
| `dict` | `{"name": "Kartik"}` |
| `NoneType` | `None` |

---

## 4. String (`str`)

Used to store text.

```python
name = "Kartik"
city = "Bangalore"
```

Check the type:

```python
print(type(name))
```

Output:

```text
<class 'str'>
```

---

## 5. Integer (`int`)

Used for whole numbers.

```python
age = 23
servers = 5
```

Example:

```python
print(type(age))
```

---

## 6. Float (`float`)

Used for decimal numbers.

```python
price = 99.50
cpu_usage = 75.5
```

---

## 7. Boolean (`bool`)

Boolean values can be:

```python
True
False
```

Example:

```python
server_running = True
deployment_successful = False
```

---

## 8. List (`list`)

A list stores multiple values and is mutable.

```python
servers = ["web01", "web02", "web03"]
```

Access an item:

```python
print(servers[0])
```

Output:

```text
web01
```

Modify a list:

```python
servers[0] = "web-server"
```

---

## 9. Tuple (`tuple`)

A tuple stores multiple values but cannot be modified after creation.

```python
ports = (80, 443, 22)
```

---

## 10. Set (`set`)

A set stores unique values.

```python
languages = {"Python", "Bash", "Python"}
print(languages)
```

Duplicate values are removed.

---

## 11. Dictionary (`dict`)

A dictionary stores data as key-value pairs.

```python
server = {
    "name": "web01",
    "ip": "10.0.0.10",
    "status": "running"
}
```

Access a value:

```python
print(server["name"])
```

Output:

```text
web01
```

Dictionaries are extremely useful in automation and API responses.

---

## 12. NoneType

`None` represents the absence of a value.

```python
result = None
```

---

# 13. Checking Data Types

Use the `type()` function:

```python
name = "Kartik"
age = 23
salary = 22500.50
is_working = True

print(type(name))
print(type(age))
print(type(salary))
print(type(is_working))
```

---

# 14. Type Conversion

Python allows values to be converted between compatible types.

### String → Integer

```python
age = "23"
age = int(age)
```

### Integer → String

```python
age = 23
age = str(age)
```

### String → Float

```python
price = "99.50"
price = float(price)
```

---

# 15. DevOps Example

Variables and data types are heavily used in automation.

```python
server_name = "web01"
server_ip = "10.0.0.10"
server_port = 443
server_running = True

server = {
    "name": server_name,
    "ip": server_ip,
    "port": server_port,
    "running": server_running
}

print(server)
```

This type of structure becomes useful when working with:

- Cloud APIs
- Server information
- Configuration data
- JSON
- Automation scripts

---

# Key Takeaways

- Variables store values.
- Python is dynamically typed.
- `str` stores text.
- `int` stores whole numbers.
- `float` stores decimal numbers.
- `bool` stores `True` or `False`.
- Lists are mutable.
- Tuples are immutable.
- Sets store unique values.
- Dictionaries store key-value pairs.
- `type()` identifies a value's type.
- Python supports type conversion.
