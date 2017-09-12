## Girl Scout Cookie Order

We have all been there, the irresistible face of a cute kid selling tasty cookies. They're everywhere...
at the store, knocking on the door, in the parking lot...
Your objective is to create an ArrayList project that keeps track of the variety of cookie you ordered and the quantity. You will also
keep track of your total number of boxes purchased. You are going to give the program the ability to remove a variety from the list
just remember this may make the girl scout sad so please be kind.

### The `CookieOrder` Class
- Wite this class to keep track of 2 pieces of instance data: `variety` of cookie and `numBoxes` purchased
- Create the constructor to handle this data and 2 accessor methods

### The `MasterOrder` Class will maintain a list of cookies being purchased
- Declare your ArrayList and name it `orders`
- Create a construcor and the following methods
- `public void addOrder(CookieOrder theOrder)` add an order to the list showing variety and quantity
- `public int getTotalBoxes()` keep track of total boxes ordered
- `public int removeVariety(String variety)` give the ability to pick out a variety of cookie and remove
   it from the list (keep track of total boxes removed as well)

### The `OrderApp` Class 
- Add 4 orders
- Total the boxes purchased
- Remove an order
- Re-total the boxes purchased

### Example
```bash
Current Order
Variety: Tagalongs Boxes: 1
Variety: Thin Mints Boxes: 5
Variety: Samoas Boxes: 2
Variety: Tagalongs Boxes: 3
 
You have ordered 11 boxes

You are removing 3 boxes
Current Order
Variety: Tagalongs Boxes: 1
Variety: Thin Mints Boxes: 5
Variety: Tagalongs Boxes: 3
```
