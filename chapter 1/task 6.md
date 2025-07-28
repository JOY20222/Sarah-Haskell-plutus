 define a function `addNumbers` which takes two integers and returns their sum:

```haskell
-- Define the function
addNumbers :: Int -> Int -> Int
addNumbers x y = x + y

-- Main function to run and test addNumbers
main :: IO ()
main = do
    let a = 10
    let b = 20
    let result = addNumbers a b
    putStrLn ("The sum of " ++ show a ++ " and " ++ show b ++ " is " ++ show result)
```

### How to Run:

1. Save the code in a file named `AddNumbers.hs`.
2. Compile it with GHC:

   ```bash
   ghc AddNumbers.hs
   ```
3. Run the executable:

   ```bash
   ./AddNumbers
   ```

### Output:

```
The sum of 10 and 20 is 30
```



