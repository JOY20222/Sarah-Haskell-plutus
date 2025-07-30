```haskell
-- Define the function
squareArea :: Num a => a -> a
squareArea side = side * side

-- Example usage
main :: IO ()
main = do
    print (squareArea 5)       -- 25 (Int)
    print (squareArea 3.5)     -- 12.25 (Double)
    print (squareArea 2.0)     -- 4.0 (Float or Double)
```

---

### 💡 Explanation:

* The type signature:

  ```haskell
  squareArea :: Num a => a -> a
  ```

  means that `squareArea` takes a number `a` (from any type that is an instance of `Num`, such as `Int`, `Float`, or `Double`) and returns a number of the same type.
* The implementation uses `side * side` to compute the area.
* The `main` function shows example calls with different numeric types.

---

You can compile and run the code using:

```bash
ghc SquareArea.hs -o square
./square
