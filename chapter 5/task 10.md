```haskell
-- Define the function
anySquareGreaterThan50 :: [Int] -> Bool
anySquareGreaterThan50 = any (> 50) . map (^2)

-- Example usage in main
main :: IO ()
main = do
    print (anySquareGreaterThan50 [2, 5, 6])    -- False (4, 25, 36)
    print (anySquareGreaterThan50 [3, 8, 9])    -- True (9, 64, 81)
    print (anySquareGreaterThan50 [])           -- False
```

---

### 🧠 Explanation

* `map (^2)` — squares each element in the list.
* `any (> 50)` — checks if **any** element in the list is greater than 50.
* So, `any (> 50) . map (^2)` — **first squares** all elements, **then checks** if any result is greater than 50.

This is a **point-free** style: no need to explicitly pass the list as a parameter.

---

### 🔍 How It Works Internally

Example:

```haskell
anySquareGreaterThan50 [3, 8, 9]
-- map (^2) [3,8,9] = [9,64,81]
-- any (> 50) [9,64,81] = True
