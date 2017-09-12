## Creating a Shopping Cart using the ArrayList class

### The Item Class

Create an **Item** class that models an Item to be purchased. It should contain instance data and a constructor to hold the following characteristics: name, price and quantity. Item class should also include accessor methods for the 3 characteristics and a toString summary.

### The ShopApp Class

Create an ArrayList from the Item class...call your ArrayList `items`. Here is an example of a previous ArrayList declaration that we programmed : `ArrayList<String>ingredients = new ArrayList<String>();`

The **ShopApp** class should be designed to model shopping in similar fashion to Amazon and other online sites (where you can add to cart and you will see your total increase with each item added). Run a do while loop to simulate shopping, having the user enter the item, quantity and price (you will need variables for these). Store the items in an ArrayList and update the total due at checkout.

 **Stretch task**: Provide an opportunity to remove an item from the shopping cart if a user no longer desires to make that particular purchase.

#### Examples

```bash
Enter the name of the item: Shoes
Enter the unit price: 25
Enter the quantity: 2

Current Cart
Item: Shoes		  Price: 25.0	    Quantity: 2
Total Price: $50.00

Continue shopping (y/n)? y
Enter the name of the item: Shirt
Enter the unit price: 15
Enter the quantity: 3

Current Cart
Item: Shoes		  Price: 25.0	    Quantity: 2		
Item: Shirt		  Price: 15.0	    Quantity: 3		
Total Price: $95.00

Continue shopping (y/n)? n
```
