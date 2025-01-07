# Create A Catalog Calculator Using Loop And Dictionary Methods With Python

#Introduction 
When working with several products, companies need a way to track the cost of each item. With the Python dictionary method, you can easily associate an item with its exact cost. Using a loop, you can prompt customers to specify each item they would like to purchase until they indicate they are done ordering, allowing you to calculate the total cost.
## Why use the Loop and Dictionary method? 
Although there are several ways to associate an object or item with an exact cost, I chose to use a dictionary and a loop for several reasons. First, it is essential that my code remains simple and efficient. When companies deploy new code, they want it to be easy to understand and maintain, particularly for other developers who may need to update it in the future.

By using a dictionary to map items directly to their prices, the code becomes highly readable and intuitive. Each item in the dictionary has an associated price, making it easy for anyone reading the code to see the relationship between the products and their prices.

The loop method is used to repeatedly prompt the user for input and process their selections. By using a while True loop, I can continuously ask the customer for an item until they specify they are done ordering. This makes it simple to accumulate the total cost of the selected items while ensuring the program can handle multiple inputs without interruption.
## Use Case
In this example, a technology company sells equipment to other businesses. The company has asked me to create a block of code that will allow their website to prompt users for the items they are considering purchasing in order to provide a rough estimate of the total cost at checkout.

 ```
#define dictonary
Catalog = {
    "Macbook": 1000.25,
    "Headset": 27.50,
    "Keyboard": 38.50,
    "Ipad": 1100.00,
    "Desktop": 1008.50,
    "Mouse": 18.50,
 
}
#Set total_amount to 0
total_amount = 0
#Loop Forever
while True:
 try:
    #Get User input
    item = input("Item: ").title()
    #Check if item is in dictonary
    if item in catalog:
      #Add total item price
      total_amount += catalog[item]
      #Print total_amount
      print("Total: $", end="")
      print("{:.2f}".format(total_amount))
 except EOFError:
       # Break out of loop
       print()
       break

 ```
#Why Use a Dictionary and Loop?
Dictionary for Item-Price Mapping:

A dictionary provides a clear and efficient way to store and retrieve product prices. The keys are the item names, and the values are the corresponding prices. This allows for easy lookups with constant-time complexity (O(1)).
Using a dictionary makes the code more readable, as it directly maps an item to its price. If the company needs to update product prices in the future, they can simply modify the dictionary without needing to change the rest of the logic.
Loop for Repeated Input:

The while True loop allows for continuous user input until the user chooses to stop. This is ideal in a shopping scenario, where the user may want to add multiple items to their cart in a single session.
The loop keeps the process simple, as it doesn't require any complex exit conditions. The EOFError exception is used to break out of the loop when the user indicates they are finished (e.g., by pressing Ctrl+D or entering an end-of-file signal).
This approach ensures that the program keeps running until the customer is done entering items, making the process seamless for the user.
Efficiency and Clarity:

The code is designed to be as simple as possible, while still being highly effective. Using the dictionary method allows for quick and efficient lookups of product prices, while the loop method enables repetitive interactions with the user without redundant code.
