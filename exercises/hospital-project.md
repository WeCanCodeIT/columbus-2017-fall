## High St. Hospital

### Objective

- Students will employ good software design and testing principles in order to create a class hierarchy using APIE (Abstraction, Polymorphism, Inheritance and Encapsulation).
- Students will be able to define **super**, **abstract**, **extends**, **implements** and **is-a**

## The Scenario

High St. Hospital is an organizational mess.  They have unkempt files of employee information scattered throughout manilla folders, computer data files, and old tin filing cabinets (ok ok so its not 1992...but we needed a situation!).  With the madness of the daily grind, patients are the priority.  But the upmost care cannot be given to the patients if the hospital is disorganized.  High St. Hospital wants to get it together.  They have subcontracted We Can Code IT full-stack apprentices (who work for the reasonably inexpensive price of free) to come in and organize.  They enable you to set up shop with a few company laptops in an old dissheveled break room.  Your mission is to create a set of classes that contain information on the employees at Hammond Hospital:

**High St. Hospital has the following generic model at its facility:**
-	`HospitalEmployee`
      - initializes `patientHealth = 10` 
      -  `getPay()` abstract method with no specifications
      - appropriate getter methods and toString() 
      
**High St. Hospital has the following classifications at its facility**
-	Doctor is a type of Hospital Employee and gets paid 90,000
-	Nurse is a type of Hospital Employee and gets paid 50,000
-	Surgeon is a type of Doctor and gets paid 120,000
-	Receptionist is a type of Hospital Employee and gets paid 45,000
-	Janitor is a type of Hospital Employee and gets paid 40,000



## The Data
The following **Instance Data** will need to be taken care of for each employee

- **`HospitalEmployee`**: Employee Name, Employee Number
- **`Doctor`**: Employee Name, Employee Number, Specialty Area (Heart, Brain, Foot, etc…)
- **`Surgeon`**: Employee Name, Employee Number, Specialty Area, and whether they are operating or not)
- **`Nurse`**: Employee Name, Employee Number, and Number of Patients they are taking care of
- **`Receptionist`**: Employee Name, Employee Number, whether they are on the phone or not
- **`Janitor`**: Employee Name, Employee Number, whether they are sweeping or not

## Special Duties
Not all employees in the hospital have the same capabilities. Only certain staff members can **implement** **`MedicalDuties`** such as `drawBlood()` and `careForPatient()`




### Part 1 

Let's get organized.  Your team is meeting for the first time at High St. Hospital.  Programming at this time is out of the question.  You need to get a feel for the task at hand.  You do not even want to create an algorithm yet.  

Diagram the classes you will need for this program.  What are the inheritance relationships?  How and where does the problem tell you this information?

### Part 2

Let's prepare a project where we can test drive information 

### Part 3

We can stare at this stuff all we want but until we actually make some software, High St. Hospital will have patients that are not being served with the best possible care. Time is of the essence! Hurry up, but take your time...

#### Our first iteration of this new software...

```bash
High St. Hospital Employees: 
Michael	234	Heart
Vincent	645	Brain		true
Sonny	789	6
Luca	375	Business
Tom	951	Office		true
Anthony	123	Maintenence	false

Vincent is operating now.
Tom is on the phone now.
Anthony is not sweeping now.
```

### Part 4
- Using Polymorphism let's pay our employees (getPaid() method)
- Stretch task: Place our employees in a collection
- Stretch task: Through user input, type search for an employee by name and access their info/what they are doing
