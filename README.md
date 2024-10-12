# **Module: Temperature Conversion and Name Filtering**

This module provides several utility functions, including converting temperatures between Celsius and Fahrenheit, applying a hash to a temperature, filtering and processing names and numbers, and validating passwords based on specified security criteria.

---

## **Functions**

### **1. `celsius_to_fahrenheit(celsius)`**
Converts a temperature from Celsius to Fahrenheit.

#### **Args**:
- `celsius (float)`: Temperature in degrees Celsius.

#### **Returns**:
- `float`: Temperature converted to degrees Fahrenheit.

#### **Example**:
```python
celsius = 25
fahrenheit = celsius_to_fahrenheit(celsius)
print(fahrenheit)  # Output: 77.0
```

---

### **2. `fahrenheit_to_celsius(fahrenheit)`**
Converts a temperature from Fahrenheit to Celsius.

#### **Args**:
- `fahrenheit (float)`: Temperature in degrees Fahrenheit.

#### **Returns**:
- `float`: Temperature converted to degrees Celsius.

#### **Example**:
```python
fahrenheit = 77
celsius = fahrenheit_to_celsius(fahrenheit)
print(celsius)  # Output: 25.0
```

---

### **3. `apply_hash(temperature)`**
Applies a hash function to a temperature value.

#### **Args**:
- `temperature (float)`: The temperature to be hashed.

#### **Returns**:
- `int`: The hash value corresponding to the temperature.

#### **Example**:
```python
celsius = 25
fahrenheit = celsius_to_fahrenheit(celsius)
temperature_hash = apply_hash(fahrenheit)
print(temperature_hash)
```

---

### **4. `process_names_and_numbers(names, numbers)`**
Filters names with more than 5 characters and squares the corresponding numbers.

#### **Args**:
- `names (list of str)`: List of names.
- `numbers (list of int/float)`: List of numbers corresponding to the names.

#### **Returns**:
- `tuple`: A tuple containing two lists:
  - A list of names that have more than 5 characters.
  - A list of squared numbers corresponding to the filtered names.

#### **Example**:
```python
names = ["Ana", "Sebastian", "Luis", "Marcela", "Pedro"]
numbers = [3, 7, 2, 9, 5]

filtered_names, squared_numbers = process_names_and_numbers(names, numbers)
print(filtered_names)  # Output: ['Sebastian', 'Marcela']
print(squared_numbers)  # Output: [49, 81]
```

---

### **5. `validate_password(password)`**
Validates whether a password meets specific security criteria:
- Minimum of 8 characters.
- Contains at least one uppercase letter.
- Contains at least one lowercase letter.
- Contains at least one numeric digit.

#### **Args**:
- `password (str)`: The password to be validated.

#### **Returns**:
- `bool`: `True` if the password is valid, `False` otherwise.

#### **Example**:
```python
password = "!passwordSecured$48?2003"
is_valid = validate_password(password)
if is_valid:
    print(f"The password '{password}' is valid.")
else:
    print(f"The password '{password}' is not valid.")
```

---

### **Imports**
- `re`: This module is used to apply regular expressions for validating the password.
