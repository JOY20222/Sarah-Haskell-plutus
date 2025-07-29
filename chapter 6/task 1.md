```haskell
-- Define the factorial function using recursion
factorial :: Integer -> Integer
factorial 0 = 1                            -- Base case: factorial of 0 is 1
factorial n
  | n > 0     = n * factorial (n - 1)      -- Recursive case: n * factorial(n - 1)
  | otherwise = error "Negative input!"   -- Error case: factorial is undefined for negative numbers

-- Main function to test the factorial function
main :: IO ()
main = do
  putStrLn "Enter a number:"
  input <- getLine
  let number = read input :: Integer
  if number < 0
    then putStrLn "Factorial is not defined for negative numbers."
    else putStrLn ("Factorial is: " ++ show (factorial number))
```

---

### 🔍 Explanation

1. **Function Signature**:

   ```haskell
   factorial :: Integer -> Integer
   ```

   This says the `factorial` function takes an `Integer` and returns an `Integer`.

2. **Base Case**:

   ```haskell
   factorial 0 = 1
   ```

   Factorial of 0 is defined as 1.

3. **Recursive Case**:

   ```haskell
   factorial n
     | n > 0     = n * factorial (n - 1)
   ```

   If `n` is greater than 0, we recursively call `factorial (n - 1)` and multiply by `n`.

4. **Error Handling**:

   ```haskell
     | otherwise = error "Negative input!"
   ```

   If the input is negative, an error is thrown (factorial isn't defined for negative numbers).

5. **Main Function**:
   The `main` function gets user input, converts it to `Integer`, and prints the factorial using the `factorial` function.

---

### 🧪 How to Run

1. Save the code to a file, e.g., `Factorial.hs`.
2. Compile or run it using GHC:

   ```bash
   ghc Factorial.hs -o factorial
   ./factorial
   ```

   Or run it directly using:

   ```bash
   runhaskell Factorial.hs
   ```
