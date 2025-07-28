```haskell
-- Function to calculate area of a circle
circleArea :: Float -> Float
circleArea r = pi * r * r

-- Function to find the maximum of three Ints
maxOfThree :: Int -> Int -> Int -> Int
maxOfThree a b c = max a (max b c)

-- Main function to test the above
main :: IO ()
main = do
    -- Test circleArea
    let radius1 = 5.0
    let radius2 = 2.5
    putStrLn ("circleArea 5.0 = " ++ show (circleArea radius1))
    putStrLn ("circleArea 2.5 = " ++ show (circleArea radius2))

    -- Test maxOfThree
    let max1 = maxOfThree 10 20 15
    let max2 = maxOfThree (-5) (-1) (-10)
    let max3 = maxOfThree 100 100 100
    putStrLn ("maxOfThree 10 20 15 = " ++ show max1)
    putStrLn ("maxOfThree (-5) (-1) (-10) = " ++ show max2)
    putStrLn ("maxOfThree 100 100 100 = " ++ show max3)
```

---

### 🔧 How to Run:

1. Save the code in a file named `CircleAndMax.hs`.
2. Compile it:

   ```bash
   ghc CircleAndMax.hs
   ```
3. Run:

   ```bash
   ./CircleAndMax
   ```

---

### ✅ Sample Output:

```
circleArea 5.0 = 78.53982
circleArea 2.5 = 19.634954
maxOfThree 10 20 15 = 20
maxOfThree (-5) (-1) (-10) = -1
maxOfThree 100 100 100 = 100
```
