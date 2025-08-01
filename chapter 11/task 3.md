```haskell
main :: IO ()
main = do
    putStrLn "Enter a number:"
    input <- getLine
    let number = read input :: Int
    let result = number * 2
    putStrLn ("The result is: " ++ show result)
```

---

### 🧠 Explanation:

* `putStrLn` prints a prompt.
* `getLine` reads the user input as a `String`.
* `read input :: Int` converts the string input to an integer.
* `number * 2` multiplies it by 2.
* `show result` converts the result back to a string for display.

---

### ✅ Example:

**Input:**

```
Enter a number:
5
```

**Output:**

```
The result is: 10
```

---

### ▶️ Running the Program:

**Option 1: Compile and run**

```bash
ghc Main.hs -o multiply
./multiply
```

**Option 2: Run in GHCi**

```bash
ghci Main.hs
main
