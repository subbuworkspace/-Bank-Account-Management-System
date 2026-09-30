# 🏦 Bank Account Management System using Python OOP

A beginner-friendly **Bank Account Management System** built using **Python Object-Oriented Programming (OOP)** concepts(all data are dumm3qqqq111111111111111).

This project demonstrates how OOP concepts can be applied to a real-world banking scenario such as creating accounts, depositing money, withdrawing money, checking balances, and displaying account information.

---

## 📌 Project Overview

The project contains two types of bank accounts:

* **BankAccount** – Base/parent class
* **SavingsAccount** – Child class inherited from `BankAccount`

The project demonstrates:

* Classes
* Objects
* Constructors
* Instance Variables
* Class Variables
* Encapsulation
* Inheritance
* Polymorphism
* Methods
* `super()`

---

## 🎯 Objectives

The main objectives of this project are:

1. Understand the fundamentals of Python OOP.
2. Create classes and objects.
3. Use constructors to initialize objects.
4. Implement encapsulation using private variables.
5. Implement inheritance.
6. Understand method overriding and polymorphism.
7. Build a small real-world application using OOP.

---

# 🧠 OOP Concepts Used

## 1. Class

A class is a blueprint used to create objects.

```python
class BankAccount:
    pass
```

Here, `BankAccount` is a class.

---

## 2. Object

An object is an instance of a class.

```python
account1 = BankAccount(
    "Subrata",
    "ACC1001",
    10000
)
```

Here, `account1` is an object of the `BankAccount` class.

---

## 3. Constructor

The `__init__()` method is used to initialize object attributes.

```python
def __init__(self, account_holder, account_number, balance):
    self.account_holder = account_holder
    self.account_number = account_number
    self.__balance = balance
```

The constructor is automatically called when an object is created.

---

# 🔐 4. Encapsulation

Encapsulation means keeping data and methods together inside a class and controlling access to the data.

In this project:

```python
self.__balance = balance
```

The double underscore makes `balance` a private attribute.

Instead of directly modifying the balance, we use methods:

```python
account1.deposit(5000)

account1.withdraw(3000)
```

This provides controlled access to the account balance.

---

# 👨‍👩‍👦 5. Inheritance

Inheritance allows a child class to reuse properties and methods from a parent class.

```python
class SavingsAccount(BankAccount):
```

Here:

```text
BankAccount
     ↓
SavingsAccount
```

`SavingsAccount` inherits from `BankAccount`.

---

# 🔄 6. Polymorphism

Polymorphism means the same method name can have different implementations.

The parent class contains:

```python
def display_details(self):
```

The child class also defines:

```python
def display_details(self):
```

The child class overrides the parent implementation.

```python
def display_details(self):
    super().display_details()
    print("Interest Rate:", self.interest_rate, "%")
```

---

# 🧬 7. `super()`

`super()` is used to access methods or attributes from the parent class.

Example:

```python
super().__init__(
    account_holder,
    account_number,
    balance
)
```

This calls the constructor of the `BankAccount` class.

---

# 🏗️ Project Structure

```text
Bank_OOP_Project/
│
├── bank_account.py
├── README.md
└── requirements.txt
```

### `bank_account.py`

Contains the complete Python implementation of the banking system.

### `README.md`

Project documentation.

### `requirements.txt`

External dependencies required by the project.

This project doesn't require any external Python libraries.

---

# ⚙️ Technologies Used

| Technology    | Purpose              |
| ------------- | -------------------- |
| Python        | Programming language |
| OOP           | Application design   |
| Classes       | Creating objects     |
| Inheritance   | Code reuse           |
| Encapsulation | Data protection      |
| Polymorphism  | Method overriding    |

---

# ▶️ How to Run

## Step 1: Clone the repository

```bash
git clone https://github.com/your-username/Bank_OOP_Project.git
```

## Step 2: Navigate to the project

```bash
cd Bank_OOP_Project
```

## Step 3: Run the Python program

```bash
python bank_account.py
```

---

# 💻 Example

Create a normal bank account:

```python
account1 = BankAccount(
    "Subrata",
    "ACC1001",
    10000
)
```

Deposit money:

```python
account1.deposit(5000)
```

Withdraw money:

```python
account1.withdraw(3000)
```

Check balance:

```python
print(account1.get_balance())
```

Create a savings account:

```python
account2 = SavingsAccount(
    "Rahul",
    "ACC1002",
    20000,
    6.5
)
```

---

# 📊 Sample Output

```text
----- Account Details -----
Bank: ABC Bank
Account Holder: Subrata
Account Number: ACC1001
Balance: ₹ 10000

₹5000 deposited successfully.
₹3000 withdrawn successfully.

Current Balance: 12000
```

Savings account:

```text
----- Account Details -----
Bank: ABC Bank
Account Holder: Rahul
Account Number: ACC1002
Balance: ₹ 20000
Interest Rate: 6.5 %

₹5000 deposited successfully.
₹2000 withdrawn successfully.

Current Balance: 23000
```

---

# 🚨 Validation

The project also handles basic validation.

### Invalid deposit

```python
if amount > 0:
```

### Invalid withdrawal

```python
if amount <= 0:
```

### Insufficient balance

```python
elif amount > self.__balance:
    print("Insufficient balance.")
```

---

# 🌍 Real-World OOP Mapping

The project can be related to a real banking application:

```text
Bank
 │
 ├── BankAccount
 │      ├── account_holder
 │      ├── account_number
 │      └── balance
 │
 └── SavingsAccount
        ├── interest_rate
        └── account operations
```

A real banking application could further extend this design with:

* Current Account
* Savings Account
* Fixed Deposit
* Loan Account
* Customer Management
* Transaction History
* Interest Calculation
* ATM Operations
* Authentication
* Database Integration

---

# 🎯 OOP Concepts Summary

| OOP Concept   | Implementation                |
| ------------- | ----------------------------- |
| Class         | `BankAccount`                 |
| Object        | `account1`                    |
| Constructor   | `__init__()`                  |
| Encapsulation | `__balance`                   |
| Inheritance   | `SavingsAccount(BankAccount)` |
| Polymorphism  | `display_details()`           |
| Method        | `deposit()`, `withdraw()`     |
| `super()`     | Parent constructor/method     |

---

# 💡 Possible Future Enhancements

This project can be extended into a more complete banking application.

### Version 2

* Add transaction history
* Add account creation
* Add account deletion
* Add multiple customers
* Add PIN authentication

### Version 3

* Add SQLite/MySQL database
* Create login system
* Build Streamlit frontend
* Add transaction dashboard

### Version 4

Build a complete:

```text
Python OOP
     ↓
Database
     ↓
Backend
     ↓
Streamlit
     ↓
Banking Dashboard
```

---

# 🎤 Interview Questions

### Beginner

**1. What is OOP?**

OOP stands for Object-Oriented Programming. It is a programming approach based on objects and classes.

**2. What is a class?**

A class is a blueprint for creating objects.

**3. What is an object?**

An object is an instance of a class.

**4. What is `self`?**

`self` refers to the current object.

**5. What is `__init__()`?**

It is a constructor that initializes an object's attributes.

---

### Intermediate

**6. What is encapsulation?**

Encapsulation combines data and methods inside a class and controls access to the data.

**7. What is inheritance?**

Inheritance allows a child class to reuse functionality from a parent class.

**8. What is polymorphism?**

Polymorphism allows the same method or interface to behave differently for different objects.

**9. What is method overriding?**

When a child class provides its own implementation of a method already defined in the parent class, it is called method overriding.

**10. What is `super()`?**

`super()` is used to access functionality from the parent class.

---

# 🚀 Learning Outcome

After completing this project, you should be able to explain and implement the core Python OOP concepts:

```text
Class
  ↓
Object
  ↓
Constructor
  ↓
Encapsulation
  ↓
Inheritance
  ↓
Polymorphism
  ↓
Real-World Application
```

---

## 👨‍💻 Author

**Subrata Mondal**

Python | Data Analytics | Data Science | Machine Learning | AI

---

⭐ If you find this project useful, consider giving the repository a star!
