```haskell
-- Define describeTuple to extract and describe tuple contents
describeTuple :: (Int, String) -> String
describeTuple (num, text) = "The number is " ++ show num ++ " and the text is \"" ++ text ++ "\"."

-- Main function to test describeTuple
main :: IO ()
main = do
    putStrLn $ describeTuple (42, "hello")
    putStrLn $ describeTuple (7, "Haskell")
    putStrLn $ describeTuple (100, "functional programming")
```

---

### 🔧 How to Run:

1. Save the code in a file named `DescribeTuple.hs`
2. Compile it with GHC:

   ```bash
   ghc DescribeTuple.hs
   ```
3. Run the compiled program:

   ```bash
   ./DescribeTuple
   ```

---

### ✅ Example Output:

```
The number is 42 and the text is "hello".
The number is 7 and the text is "Haskell".
The number is 100 and the text is "functional programming".
