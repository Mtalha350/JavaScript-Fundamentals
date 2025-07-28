# CHALLENGE #4

Steven needs a simple tip calculator for dining at restaurants. In his country, the tipping rule is as follows:

- If the bill is between **50 and 300**, the tip is **15%**.
- Otherwise, the tip is **20%**.

## Tasks:

1. **Calculate the Tip**:

   - Create a variable `tip` to store the tip amount.
   - Do **not** use an `if...else` statement (you may start with one, but must convert it to a ternary operator).

2. **Print Output to Console**:

   - The output should include the **bill amount**, **tip**, and **total (bill + tip)**.

   **Example Output:**

   ```
   The bill was 275, the tip was 41.25, and the total value 316.25.
   ```

   - Use variables for `bill` and `tip` to construct the string (do not hard-code values).

## Test Data:

- Bill values to test: **275, 40, 430**.

## Hints:

- **To calculate 20% of a value:** multiply by `0.2` (i.e., `value * 20/100`).
- **A number X is between 50 and 300 if:** `X >= 50 && X <= 300`.

Good luck! 🚀
