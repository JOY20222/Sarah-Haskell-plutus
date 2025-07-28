 ```haskell
-- Define the applyTwice function
applyTwice :: (a -> a) -> a -> a
applyTwice f x = f (f x)

-- Example usage in main
main :: IO ()
main = do
    -- Example 1: Double a number twice
    let result1 = applyTwice (*2) 3
    putStrLn ("applyTwice (*2) 3 = " ++ show result1)  -- Output: 12

    -- Example 2: Add 1 twice
    let result2 = applyTwice (+1) 5
    putStrLn ("applyTwice (+1) 5 = " ++ show result2)  -- Output: 7

    -- Example 3: Reverse a string twice (returns original)
    let result3 = applyTwice reverse "hello"
    putStrLn ("applyTwice reverse \"hello\" = " ++ show result3)  -- Output: "hello"
```

### Explanation:

* `applyTwice` takes a function `(a -> a)` and a value `a`, then applies the function to the value **twice**.
* This works for any type `a` where the function is applicable (e.g., numbers, strings, lists).

### How to Run:

1. Save as `ApplyTwice.hs`
2. Compile:

   ```bash
   ghc ApplyTwice.hs
   ```
3. Run:

   ```bash
   ./ApplyTwice
   ```

### Output:

```
applyTwice (*2) 3 = 12
applyTwice (+1) 5 = 7
applyTwice reverse "hello" = "hello"
```
