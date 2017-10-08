## Creating a Shopping Cart using the ArrayList class

### The Item Class

Create an **`Item`** class that models an Item to be purchased. It should contain instance data and a constructor to hold the following characteristics: `String name`, `double price` and `int quantity`. Item class should also include accessor methods for the 3 characteristics and a toString summary.

### The Order Class

Create an **`Order`** class that maintains the `ArrayList items`. This class will contain behaviors to `addItem`, `removeItem` by name and display the `currentOrder`. 

### The ShopApp Class

- When you prompt the user for the name of item, quantity and price, store these in an ole fashion `Item` object.
- Once you have that `Item` object, go ahead and **`add`** it to your `ArrayList`
- Need to display the items that are currently in your shopping cart? Go ahead and do that 

The `ShopApp` class should be designed to model shopping in similar fashion to Amazon and other online sites (where you can add to cart and you will see your total increase with each item added). Use a loop to simulate shopping, asking the user to enter the item, quantity and price. (You will need variables for these.) Store the items in an `ArrayList` and update the total due at checkout.



#### Examples

```bash
Welcome to We Can Code ITs online store
Enter the name of the item:
Sunglasses
Enter the price of the item:
100
Enter the quantity: 
1
Current Cart
Item: Sunglasses Price: 100.0 Quantity: 1.0
Total Price: 100.0
Continue Shopping? (y/n)
y
Enter the name of the item:
Shoes
Enter the price of the item:
50
Enter the quantity: 
2
Current Cart
Item: Sunglasses Price: 100.0 Quantity: 1.0
Item: Shoes Price: 50.0 Quantity: 2.0
Total Price: 200.0
Continue Shopping? (y/n)
y
Enter the name of the item:
Shirt
Enter the price of the item:
10
Enter the quantity: 
3
Current Cart
Item: Sunglasses Price: 100.0 Quantity: 1.0
Item: Shoes Price: 50.0 Quantity: 2.0
Item: Shirt Price: 10.0 Quantity: 3.0
Total Price: 230.0
Continue Shopping? (y/n)
n
Would you like to remove anything from your cart?(y/n)
y
Enter the name of the item you would like to remove.
Sunglasses
You are removing Sunglasses
Would you like to remove anything else?(y/n)
y
Enter the name of the item you would like to remove.
Shoes
You are removing Shoes
Would you like to remove anything else?(y/n)
n
Thanks for shopping with us!
Here is your final cart:
Item: Shirt Price: 10.0 Quantity: 3.0
Total Price: 30.0
```
