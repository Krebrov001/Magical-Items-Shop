# Verlin's Magical Items Shop

The provided code is a High-Level Assembly (HLA) program for a text-based interface simulating a magical items shop where users can browse items, make purchases, and manage transactions. Here's a comprehensive overview of its functionality and components:


### Overview

The program simulates a magical items shop named "Verlin's Magical Items Shop," offering a variety of items for adventurers. Users can view available items, select items to purchase, and complete transactions. The shop includes a dynamic inventory system, user input handling, and a checkout process.

### Major Parts and Features

#### 1. **Displaying Items for Sale**
- The shop offers seven magical items, each with a unique description, price, and quantity available. Items include Blue Sleeper Mushrooms, Amulet of Osiris, Hyperborean Greatsword, Asgardian Battle Axe, Voodoo Potion Antidote, Flying Carpet, and Herculean Strength Potion.

#### 2. **Dynamic Inventory Management**
- The program tracks the quantity of each item and updates the inventory as items are sold. It prevents selling items that are out of stock.

#### 3. **User Interaction**
- Users interact with the shop via a text-based interface, choosing items to purchase by entering the corresponding number of the item. They can also choose to checkout instead of buying more items.

#### 4. **Purchase Process**
- Users can select items to buy, and the program updates the total cost and keeps track of the number of items bought. It supports purchasing multiple quantities of the same item.

#### 5. **Checkout System**
- Upon deciding to checkout, users must enter the amount of credits they have. The program validates the input to ensure it's a positive number within a reasonable range. It calculates the total cost and handles insufficient funds scenarios.

#### 6. **Receipt Generation**
- A detailed receipt is generated listing all purchased items, quantities, and the total cost. It uses custom characters for formatting and displays the receipt clearly.

#### 7. **Change Calculation**
- Calculates change due to the user if the payment exceeds the total cost and displays it in a user-friendly manner, including breaking down the change into dollars, quarters, dimes, nickels, and pennies.

### How It Works

1. **Initialization**: Sets up constants for special characters used in the UI and initializes variables for item prices, quantities, and transaction-related data.

2. **Main Loop**: Continuously runs until the user decides to checkout, displaying items and prompting for actions.

3. **Item Selection**: Allows users to select items by entering a number. Validates input and updates inventory and purchase details accordingly.

4. **Inventory Update**: Decrements item quantities and updates the shopping cart totals as items are bought.

5. **Checkout Prompt**: Prompts the user for the amount of credits they wish to pay with, ensuring valid input through a loop.

6. **Transaction Completion**: Calculates total cost, compares it with the user's credits, and processes the transaction. Generates a detailed receipt if successful.

7. **Error Handling**: Includes robust error handling for invalid inputs during item selection and credit entry, guiding the user towards correct actions.

### Key Features

- **Dynamic UI**: The interface updates in real-time as items are bought or the inventory changes.
- **Inventory System**: Tracks item quantities and prevents selling out-of-stock items.
- **Flexible Input Handling**: Uses exceptions to manage invalid inputs gracefully, guiding users towards correct actions.
- **Detailed Receipts**: Generates itemized receipts showing what was bought, total cost, and change due in a readable format.

### Summary

This program is a comprehensive simulation of a shop transaction system, focusing on user interaction, inventory management, and dynamic UI updates. It demonstrates advanced HLA programming techniques, including file inclusion, procedure definition, exception handling, and detailed receipt generation. It's designed to be interactive and user-friendly, guiding users through transactions while preventing errors and managing inventory in real-time.

### Links to Other Documentations

- [Program Description](Program_Description.md)
- [Store Logic](Store_Logic.md)
