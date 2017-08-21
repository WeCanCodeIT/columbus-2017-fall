## ATM Machine

### Objective

Design a class and client code to simulate access and transactions that occur with an ATM Machine.  ATM Machines require the user to enter a 4 digit pin to gain access to the system. 

Control your ATM object with a 3 parameter constructor(firstName,lastName,acct#)

Make sure your ATM is able to do the following:
-	Check for an acceptable 4 digit pin
o	Allow access if the pin is correct
o	Deny access otherwise
•	Ask if the ATM is associated with user’s bank account
o	Accept if it is
o	Charge a 2.00 service fee if the ATM does not match with the users bank account
•	Allow for Deposits
•	Allow for Cash Withdrawals
•	Allow for Balance Inquiries
•	Print a summation of information at the end of all transactions for the user (toString())



#### Examples

```bash
Welcome to Bank of We Can Code IT ATM.
Please enter your pin #:
1234

Is your card associated with the WCCI ATM system?
no
Ok...you will be charged a 2.00 fee for using our system.
What would you like to do next?
 Press 1 for deposit
 Press 2 for Withdrawal
 Press 3 to Check Balance
 Press 4 to Exit

4
Thank you have a nice day!
```
