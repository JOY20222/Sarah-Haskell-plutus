```haskell
main :: IO ()
main = do
    putStrLn "Enter the first number:"
    input1 <- getLine
    putStrLn "Enter the second number:"
    input2 <- getLine
    let num1 = read input1 :: Int
    let num2 = read input2 :: Int
    let sumResult = num1 + num2
    putStrLn ("The sum is: " ++ show sumResult)
```

---

### 🧠 Explanation:

* `getLine` reads a line of input as a `String`.
* `read input1 :: Int` converts the input to an integer.
* `+` performs the addition.
* `show` converts the result back to a string for printing.

---

### ✅ Example:

**Input:**

```
Enter the first number:
5
Enter the second number:
8
```

**Output:**

```
The sum is: 13
```

---

### ▶️ How to Run:

1. Save as `Main.hs`
2. Compile and run:

   ```bash
   ghc Main.hs -o sumTwoNumbers
   ./sumTwoNumbers
   ```

Or run in GHCi:

```bash
ghci Main.hs
main
