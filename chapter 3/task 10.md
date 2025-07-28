```haskell
-- Define isPalindrome using guards and recursion
isPalindrome :: String -> Bool
isPalindrome str
    | length str <= 1 = True
    | head str == last str = isPalindrome (init (tail str))
    | otherwise = False

-- Main function to test isPalindrome
main :: IO ()
main = do
    putStrLn ("isPalindrome \"racecar\" = " ++ show (isPalindrome "racecar"))
    putStrLn ("isPalindrome \"haskell\" = " ++ show (isPalindrome "haskell"))
    putStrLn ("isPalindrome \"madam\" = " ++ show (isPalindrome "madam"))
```

---

### 🔧 How to Run:

1. Save the file as `IsPalindrome.hs`
2. Compile it:

   ```bash
   ghc IsPalindrome.hs
   ```
3. Run:

   ```bash
   ./IsPalindrome
   ```

---

### ✅ Expected Output:

```
isPalindrome "racecar" = True
isPalindrome "haskell" = False
isPalindrome "madam" = True
