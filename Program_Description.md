# Verlin's Magical Items Shop - Program Description


The "Verlin's Magical Items Shop" program contains several procedures (functions) that handle different aspects of the shop's operation, from displaying items to managing transactions. Here's a detailed description of each procedure and its purpose:

### 1. `printRowSeparator`
- **Purpose**: Prints horizontal borders that separate rows with product information in the item table.
- **How It Works**: Uses a series of loops to print special characters (`left_cross_border`, `horizontal_border`, `cross_border`, `right_cross_border`) to create a visual separator line across the console. This enhances the readability of the item list by visually separating different sections of the table.

### 2. `printTableBottom`
- **Purpose**: Prints the bottom border of the entire table.
- **How It Works**: Similar to `printRowSeparator`, but uses different characters (`bottom_left_corner`, `up_cross_border`, `bottom_right_corner`) to indicate the end of the table, providing a clear visual boundary.

### 3. `printEmptyPriceCollumns`
- **Purpose**: Fills in empty lines in the price and quantity columns for items that have descriptions spanning multiple lines.
- **How It Works**: Prints vertical borders and spaces to align the table correctly when an item's description takes up more than one line, ensuring the table's columns remain aligned.

### 4. `printFullPriceCollumns`
- **Parameters**: `item_price` (uns8), `item_quantity` (uns8)
- **Purpose**: Prints the price and quantity of an item in a neatly formatted manner.
- **How It Works**: Formats the output based on the number of characters the price and quantity take up on the screen, ensuring alignment in the table. Uses conditional logic to adjust spacing for single-digit, double-digit, and triple-digit prices and quantities.

### 5. `printTableHeader`
- **Purpose**: Prints the header for the menu table, including the shop's name and column titles.
- **How It Works**: Sets console attributes for visual appeal, then prints a decorative header with the shop's name and column titles ("Item", "Description", "Price", "# left") using special characters for borders and lines for a structured look.

### 6. `printTableRows`
- **Purpose**: Displays each item's name, description, price, and quantity available in the menu table.
- **How It Works**: Iterates through each item, printing its details in a structured format. Uses `printEmptyPriceCollumns` for items with multi-line descriptions and `printFullPriceCollumns` for price and quantity. Adjusts spacing for alignment and readability.

### 7. `chooseItemNumber`
- **Purpose**: Gets the user's choice of which item to select.
- **How It Works**: Prompts the user for input, validates it, and returns a valid row number or 0 for invalid input or to quit shopping. Handles exceptions for non-numeric input or numbers outside the valid range.

### 8. `enterUserCredits`
- **Purpose**: Prompts the user to enter how many credits they have for payment.
- **How It Works**: Uses a loop for error checking, ensuring the input is a valid `uns16` value. Continues prompting until valid input is received, displaying error messages for invalid entries.

### 9. `printReceipt`
- **Purpose**: Formats and prints the receipt for purchased items.
- **How It Works**: Clears the screen, sets console attributes for readability, and prints a detailed receipt including item names, quantities bought, and total cost. Calculates and displays the total cost and change due in a user-friendly format.

### Main Logic (`project1` procedure)
- **Purpose**: The main loop of the program, handling the shopping experience from displaying items to checkout.
- **How It Works**:
  - Clears the screen and displays the table header and rows.
  - Prompts the user to choose an item or checkout.
  - Manages item selection, updating inventory and totals.
  - Handles checkout by validating credits, calculating total cost, and printing a receipt if the purchase is valid.
  - Calculates and displays change due in fantasy currency units.

### Additional Details:
- **Inventory Management**: The program tracks the quantity of each item and updates it as items are sold. It prevents selling items that are out of stock.
- **Transaction Management**: Calculates the total cost of items bought and manages the checkout process, including validating the user's credits and calculating change.
- **User Interaction**: Uses `stdin.getu8` and `stdin.getu16` for input, with exception handling for invalid inputs.
- **Display Management**: Uses `stdout.put` for output, with `console.setAttrs` to change text attributes for visual appeal. Special characters are used for table formatting.

### Summary of Major Functions:
- **Display Functions** (`printRowSeparator`, `printTableBottom`, `printEmptyPriceCollumns`, `printTableHeader`, `printTableRows`, `printReceipt`): These functions manage the visual presentation of the shop and receipt, ensuring information is clearly and attractively displayed.
- **Input and Validation** (`chooseItemNumber`, `enterUserCredits`): Handle user input, validating choices and payment amounts to ensure correct operation.
- **Main Logic**: The `project1` procedure orchestrates the shopping experience, from item selection to checkout, including inventory updates and transaction completion.

Each function plays a specific role in either displaying information to the user, managing user input, or processing transactions, creating an interactive and user-friendly shopping experience. The program uses HLA's capabilities for console output, input handling, and arithmetic operations to simulate a magical items shop, complete with inventory management and transaction processing.

- [Return to Main Page](README.md)
