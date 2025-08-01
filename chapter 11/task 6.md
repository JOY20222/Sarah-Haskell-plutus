```haskell
import Data.Char (toUpper)

main :: IO ()
main = do
    putStrLn "Enter a line of text:"
    line <- getLine
    let upperLine = map toUpper line
    putStrLn ("Uppercase: " ++ upperLine)
```

---

### 🧠 Explanation:

* `import Data.Char (toUpper)` brings in the `toUpper` function.
* `getLine` reads a line of input.
* `map toUpper line` converts every character in the line to uppercase.
* `putStrLn` prints the result.

---

### ✅ Example:

**Input:**

```
Enter a line of text:
hello world!
```

**Output:**

```
Uppercase: HELLO WORLD!
```

---

### ▶️ How to Run:

1. Save the code in a file named `Main.hs`.
2. Compile and run:

   ```bash
   ghc Main.hs -o toUpperCase
   ./toUpperCase
   ```

Or run directly in GHCi:

```bash
ghci Main.hs
main
