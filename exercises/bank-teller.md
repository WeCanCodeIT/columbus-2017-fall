# Bank Bridge Project

## Objective

Design a `BankAccount` class that will perform capabilities of a single Bank Account, a `Bank` class that will house multiple accounts and a `BankingApp` (with a `main` method) to simulate a user interface where you can access your accounts and perform banking transactions.

### Tasks

Inside of `BankAccount` Class program the following:
- 3 instance variables to handle `String accountNum`, `String type`, and `double balance`
- note the pin will be a unique identifier
- create the `Constructor` to read in a BankAccount object
- create the following methods: `getType(), getBalance(), deposit(double amount), withdrawal(double amount)`
- be sure to update `balance` properly in deposit and withdrawal and to return the proper data in all methods

Inside of the `Bank` Class complete the following:
- Create a `map` called `accounts`
- `public Collection<BankAccount> accounts()` to return all accounts
- A `void` method to add a BankAccount
- A `BankAccount` method to access a particular `accountNum`
- A `BankAccount` method to `close` a particular `accountNum`


Inside of the `BankingApp` Class program the following:
- A `Bank` object called `myBank`
- A `BankAccount` object called `account1` with the following properties `("1111","Checking",500.00)`
- A `BankAccount` object called `account2` with the following properties `("2222","Savings",2500.00)`


