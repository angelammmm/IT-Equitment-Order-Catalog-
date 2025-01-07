# Create A Catalog Calculator Using Loop And Dictionary Methods With Python

##Introduction 
When working with several products companies need a way to keep track of how much every itme cost. With the Python Dictonary method you can easily associate an itme to an exact cost.
While using the loop method to prompt customers for every item they would like until specifying thier done ordering to calculate the totoal cost.

## Why use the Loop and Dictonmary method? 
Although thier are several wasy to associate a object or item with an exact cost. I had to keep in mind that my code needed to be simple and efficent as possible. 
When companies deploy new code they want to make sure it is easy to understand to other develkopers in case they need to updarte it later down the road. 
By defining my items directly to a price and grouping those items together readers are able to easily understand what i am attempting to acheive. And the Loop method
is used to specify if true repeat the specified action. This allows me to ask the user for input repeadidly if they meet the needed qualifications. 

## Use Case
In the following example a technology company sells equitment to other buisnesses. And has asked me to create a block of code that will allow thier website to prompt 
users for the items they are considering getting to give them a rough estiment of the end cost at check out. 

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
