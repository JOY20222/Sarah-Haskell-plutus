* `True` using `&&`
* `False` using `||`
* `True` using `not`
* A comparison expression that returns `False`

---

### ✅ Code: `BooleanExpressions.hs`

```haskell
-- Boolean expression examples

main :: IO ()
main = do
    -- True using &&
    let expr1 = True && True

    -- False using ||
    let expr2 = False || False

    -- True using not
    let expr3 = not False

    -- A comparison that returns False
    let expr4 = 5 > 10

    -- Display the results
    putStrLn ("True && True = " ++ show expr1)
    putStrLn ("False || False = " ++ show expr2)
    putStrLn ("not False = " ++ show expr3)
    putStrLn ("5 > 10 = " ++ show expr4)
```

---

### 🔧 How to Run:

1. Save the code to a file named `BooleanExpressions.hs`.
2. Compile:

   ```bash
   ghc BooleanExpressions.hs
   ```
3. Run:

   ```bash
   ./BooleanExpressions
   ```

---

### ✅ Output:

```
True && True = True
False || False = False
not False = True
5 > 10 = False
```
