# 🏦 Bank Account Management System

class BankAccount:

```
bank_name = "ABC Bank"   # Class variable

def __init__(self, account_holder, account_number, balance):
    self.account_holder = account_holder
    self.account_number = account_number
    self.__balance = balance   # Private variable

# Deposit money
def deposit(self, amount):
    if amount > 0:
        self.__balance += amount
        print(f"₹{amount} deposited successfully.")
    else:
        print("Invalid deposit amount.")

# Withdraw money
def withdraw(self, amount):
    if amount <= 0:
        print("Invalid withdrawal amount.")
    elif amount > self.__balance:
        print("Insufficient balance.")
    else:
        self.__balance -= amount
        print(f"₹{amount} withdrawn successfully.")

# Check balance
def get_balance(self):
    return self.__balance

# Display account details
def display_details(self):
    print("\n----- Account Details -----")
    print("Bank:", self.bank_name)
    print("Account Holder:", self.account_holder)
    print("Account Number:", self.account_number)
    print("Balance: ₹", self.__balance)
```

# Inheritance

class SavingsAccount(BankAccount):

```
def __init__(self, account_holder, account_number, balance, interest_rate):
    super().__init__(account_holder, account_number, balance)
    self.interest_rate = interest_rate

# Polymorphism
def display_details(self):
    super().display_details()
    print("Interest Rate:", self.interest_rate, "%")
```

# Create objects

account1 = BankAccount(
"Subrata",
"ACC1001",
10000
)

account2 = SavingsAccount(
"Rahul",
"ACC1002",
20000,
6.5
)

# Object 1 operations

account1.display_details()

account1.deposit(5000)

account1.withdraw(3000)

print("Current Balance:", account1.get_balance())

# Object 2 operations

account2.display_details()

account2.deposit(5000)

account2.withdraw(2000)

print("Current Balance:", account2.get_balance())
