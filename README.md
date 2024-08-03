# Python Challenge - Menu Challenge

## Project Summary
> This project implements a simple menu-based ordering system for a food truck. It allows users to view a menu, select items from different categories, specify quantities, and receive a summary of their order along with the total cost. The system is designed to handle nested menu structures and provides a user-friendly interface for placing orders. 

## Requirements
- Python 3. x

## How to Use the Food Truck Menu
**1. Launch the Program:** Run the script to start the ordering system.

**2. Choose a Menu Category:** You will be prompted to choose a category (e.g., Snacks, Meals, Drinks, Dessert).

```
Welcome to the variety food truck.
From which menu would you like to order?
1: Snacks
2: Meals
3: Drinks
4: Dessert
```

### Code Snippet

```
menu = {
    "Snacks": {
        "Cookie": .99,
        "Banana": .69,
        "Apple": .49,
        "Granola bar": 1.99
    },
    ...
}
```

**3. Select an Item:** After selecting a category, choose an item from the displayed list.

### Output when selecting 1 for Snacks as a category:

```
What Snacks item would you like to order?
Item # | Item name                | Price
-------|--------------------------|-------
1      | Cookie                   | $0.99
2      | Banana                   | $0.69
3      | Apple                    | $0.49
4      | Granola bar              | $1.99
```

**4. Specify Quantity:** Enter the quantity for the selected item.

```
    # Check if the customer's input is a number
    if menu_category.isdigit():
        # Check if the customer's input is a valid option
        if int(menu_category) in menu_items.keys():
            # Save the menu category name to a variable
            menu_category_name = menu_items[int(menu_category)]
            # Print out the menu category name they selected
            print(f"You selected {menu_category_name}")

            # Print out the menu options from the menu_category_name
            print(f"\nWhat {menu_category_name} item would you like to order?")
            i = 1
            menu_items = {}
            print("Item # | Item name                | Price")
            print("-------|--------------------------|-------")

```
**5. Repeat or Finalize:** You can continue ordering by repeating the steps above or finalize your order when prompted.

```
    while True:
        # Ask the customer if they would like to order anything else
        keep_ordering = input("Would you like to keep ordering? (Y)es or (N)o: ")
        # 5. Check the customer's input
        if keep_ordering.lower() == 'y':
            place_order = True
            break
        elif keep_ordering.lower() == 'n':
            place_order = False
            print("Thank you for your order")
            break
        else:
            print("Input invalid, please enter 'Y' or 'N'.")
```
### Output example for ordering 400 cookies and saying (Y)es to ordering more:
```
How many Cookie would you like to order? 968
968 x Cookie added to your order.
Would you like to keep ordering? (Y)es or (N)o: y
```
**6. Review Order:** The system will display a summary of your order along with the total cost.

## Order Summary: 
### This is an Example of the Output: 
```
This is what we are preparing for you.

Item name                  | Price  | Quantity
--------------------------|--------|----------
Cookie                     | $0.99  | 968
Burrito                    | $4.49  | 365
Soda - Large               | $2.99  | 696
Cheesecake - Strawberry    | $6.49  | 365

Your receipt total is: $7047.06
```

## Summary of How the Code Works Together
**1. Menu Structure:** A nested dictionary defines the menu categories and items with their respective prices.

**2. User Interaction:** The main loop presents the menu, allows item selection, and collects quantities.

**3. Order Management:** Selected items are stored in an order list with their details.

**4. Summary and Total:** The final order is displayed, including itemized costs and the total amount due.
