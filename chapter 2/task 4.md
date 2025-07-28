```haskell
main :: IO ()
main = do
    -- Prefix notation for infix expressions
    let sumPrefix = (+) 5 3
    let productPrefix = (*) 10 4
    let boolPrefix = (&&) True False

    putStrLn ("Using prefix notation:")
    putStrLn ("(+) 5 3 = " ++ show sumPrefix)
    putStrLn ("(*) 10 4 = " ++ show productPrefix)
    putStrLn ("(&&) True False = " ++ show boolPrefix)

    -- Infix notation for prefix functions
    let sumInfix = 7 + 2
    let productInfix = 6 * 5
    let boolInfix = True && False

    putStrLn ("\nUsing infix notation:")
    putStrLn ("7 + 2 = " ++ show sumInfix)
    putStrLn ("6 * 5 = " ++ show productInfix)
    putStrLn ("True && False = " ++ show boolInfix)
```

---

### 🔧 How to Run:

1. Save the file as `NotationExamples.hs`
2. Compile it:

   ```bash
   ghc NotationExamples.hs
   ```
3. Run:

   ```bash
   ./NotationExamples
   ```

---

### ✅ Output:

```
Using prefix notation:
(+) 5 3 = 8
(*) 10 4 = 40
(&&) True False = False

Using infix notation:
7 + 2 = 9
6 * 5 = 30
True && False = False
```
