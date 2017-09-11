# Bank Teller

## Objective

Design a `BankAccount` class that will perform capabilities of a single Bank Account, a `Bank` class that can handle a collection of Bank Accounts from multiple people and a `BankingApp` (with a `main` method) to simulate a Bank Teller being able to access accounts and perform deposits and withdrawals for people.

### Tasks

Inside of `BankAccout` Class program the following:
- 3 instance variables to handle name, balance and a pin
- note the pin will be a unique identifier
- create the `Constructor` to read in a BankAccount object
- create the following methods: `getName(), getBalance(), deposit(double amount), withdrawal(double amount)`

Insie of the `Bank` Class program the following:
- Create a `map` to keep track of multiple accounts
- Create `public Collection<BankAccount> accounts()` method
- Create `public void add(BankAccount account)` method 
