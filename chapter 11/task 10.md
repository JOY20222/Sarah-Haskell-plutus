```haskell
main :: IO ()
main = do
    putStrLn "Enter a string:"
    input <- getLine
    let reversed = reverse input
    putStrLn ("Reversed string: " ++ reversed)
```

---

### 🧠 Explanation:

* `getLine` reads a line of text from the user.
* `reverse input` uses Haskell’s built-in `reverse` function to reverse the string.
* `putStrLn` prints the reversed result.

---

### ✅ Example:

**Input:**

```
Enter a string:
hello
```

**Output:**

```
Reversed string: olleh
```

---

### ▶️ How to Run:

1. Save the code as `Main.hs`.
2. Compile and run:

   ```bash
   ghc Main.hs -o reverseString
   ./reverseString
   ```

Or run in GHCi:

```bash
ghci Main.hs
main
