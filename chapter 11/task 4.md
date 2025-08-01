```haskell
main :: IO ()
main = do
    putStrLn "Enter the first line:"
    line1 <- getLine
    putStrLn "Enter the second line:"
    line2 <- getLine
    let combined = line1 ++ line2
    putStrLn ("Concatenated result: " ++ combined)
```

---

### 🧠 Explanation:

* `getLine` reads a line of text from the user.
* `line1 ++ line2` concatenates the two strings.
* `putStrLn` prints the result.

---

### ✅ Example:

**Input:**

```
Enter the first line:
Hello,
Enter the second line:
 world!
```

**Output:**

```
Concatenated result: Hello, world!
```

---

### ▶️ Running the Program:

1. Save as `Main.hs`
2. Compile:

   ```bash
   ghc Main.hs -o concatLines
   ./concatLines
   ```

Or run in GHCi:

```bash
ghci Main.hs
main
