# Verlin's Magical Items Shop - Store Logic


## Items

Here is information about each of the items sold in the "Verlin's Magical Items Shop" program.


### 1. **Blue Sleeper Mushrooms**
   - **Price**: 8 credits
   - **Quantity Available**: Initially 12
   - **Description**: Eating one mushroom causes the consumer to go into a trance-like state of higher consciousness. Overdosage can lead to vomiting, diarrhea, fainting.

### 2. **Amulet of Osiris**
   - **Price**: 15 credits
   - **Quantity Available**: Initially 15
   - **Description**: Protects against spells and curses.

### 3. **Hyperborean Greatsword**
   - **Price**: 90 credits
   - **Quantity Available**: Initially 5
   - **Description**: Penetrates through most dragon hides.

### 4. **Asgardian Battle Axe**
   - **Price**: 120 credits
   - **Quantity Available**: Initially 8
   - **Description**: Good for bashing zombie knights.

### 5. **Voodoo Potion Antidote**
   - **Price**: 75 credits
   - **Quantity Available**: Initially 10
   - **Description**: Powerful antidote against potions prepared with voodoo black magic.

### 6. **Flying Carpet**
   - **Price**: 190 credits
   - **Quantity Available**: Initially 4
   - **Description**: Useful for battling dragons or taking princesses on dates. Will quickly take you there in style.

### 7. **Herculean Strength Potion**
   - **Price**: 240 credits
   - **Quantity Available**: Initially 2
   - **Description**: Gives you the strength of Hercules for a limited amount of time.

---

## Checkout Procedures

When the user checks out and specifies a monetary amount greater than the total cost of the purchased items, the program calculates the change due to the user by subtracting the total cost from the amount specified by the user. The change is then calculated and displayed in a fantasy monetary system, which includes dollars, quarters, dimes, nickels, and pennies, represented by special characters in the program. Here's how the process works based on the provided code:


### Monetary System and Calculation

1. **Monetary Units**:
   - The program uses a fantasy monetary system with the following units:
     - Dollar (`dollar_sign`): Represented by the character `233` (₡)
     - Quarter (`quarter_sign`): Represented by the character `244` (¼)
     - Dime (`dime_sign`): Represented by the character `229` (d)
     - Nickel (`nickel_sign`): Represented by the character `235` (₦)
     - Penny (`penny_sign`): Represented by the character `231` (¢)

2. **Calculation of Change**:
   - The change calculation starts by subtracting the total cost of the items from the user's specified credits (`user_credits`).
   - The program then calculates the change in each unit of the fantasy currency by dividing the total change by the value of each unit and using the remainder for the next unit's calculation.

### Process for Calculating Change

1. **Dollars**:
   - The total change is divided by 100 to find the number of dollars. The quotient is the number of dollars, and the remainder is used for calculating the next unit.
   - Example: If the change is 134 credits, dividing by 100 gives 1 dollar, with 34 credits remaining.

2. **Quarters**:
   - The remainder from the dollar calculation is divided by 25 (since a quarter is 25 cents). The quotient is the number of quarters, and the remainder is used for the next unit.
   - Continuing the example, 34 credits divided by 25 gives 1 quarter, with 9 credits remaining.

3. **Dimes**:
   - The remainder from the quarter calculation is divided by 10 (since a dime is 10 cents). The quotient is the number of dimes, and the remainder is used for the next unit.
   - In the example, 9 credits divided by 10 gives 0 dimes, with 9 credits remaining.

4. **Nickels**:
   - The remainder from the dime calculation is divided by 5 (since a nickel is 5 cents). The quotient is the number of nickels, and the remainder is used for the next unit.
   - In the example, 9 credits divided by 5 gives 1 nickel, with 4 credits remaining.

5. **Pennies**:
   - The remainder from the nickel calculation is considered as pennies since it's less than 5 cents.
   - In the example, 4 credits are considered as 4 pennies.

### Displaying Change

- The program displays the change due to the user in a formatted message, showing the number of each unit of currency. For example, "Your change is: 1 ₡, 1 ¼, 0 d, 1 ₦, 4 ¢".

### Handling Large Amounts

- If the user specifies an amount significantly larger than the total cost (e.g., more than the program can handle with the defined units), the program attempts to divide by 100 to calculate dollars but catches any exceptions (likely due to overflow or unsupported operations in HLA for very large numbers).
- In such cases, it clears the screen and informs the user that very large monetary quantities are not accepted, then returns the user's money without giving any change.

### Summary

- The program calculates change by sequentially dividing the total change by the value of each monetary unit, starting from the highest (dollars) to the lowest (pennies), using the remainder of each division as the dividend for the next unit.
- It uses a try-except block to handle potential errors in division, such as when the user specifies an excessively large amount, in which case it returns the money without calculating change.
- The monetary system is a simplified version of a real-world currency system, using fantasy symbols for each unit.

### Special Considerations

- The program does not explicitly handle cents as a separate unit but uses the term "pennies" for the smallest unit, directly mapping the remainder after calculating nickels to pennies.
- The division operations (`div`) are used to calculate how many of each unit can be given as change, with the remainder of each operation becoming the dividend for the next lower unit.
- The `mov` instructions are used to save the quotient (number of each unit) and prepare the remainder for the next calculation.
- The `try` and `except` block around the division by 100 for dollars is likely intended to catch errors for very large inputs, but the actual division operations for quarters, dimes, and nickels do not have explicit error handling in the provided code snippets.

### Monetary System Representation

- The monetary system is designed to mimic a real-world currency with dollars, quarters, dimes, nickels, and pennies, but uses custom symbols for each unit, likely for thematic consistency with the fantasy setting of the shop.
- The calculation assumes a direct mapping of credits to these units without a separate cent unit, simplifying the process by treating the remainder directly as pennies after calculating nickels.

### Conclusion

The change calculation is a straightforward division process, converting the total change into the largest units first and then using the remainder for subsequent units. This approach is efficient for the specified monetary system, allowing the program to provide change in a format familiar to users while fitting the fantasy theme. The use of special characters for currency symbols adds a unique touch to the transaction process, enhancing the immersive experience of shopping in a magical items shop.

- [Return to Main Page](README.md)
