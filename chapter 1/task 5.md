HC1T5 - Task 5: Laziness in Haskell

---

### ✅ Full Haskell Code

```haskell
-- File: InfiniteNumbers.hs

-- Generates an infinite list of natural numbers starting from 1
infiniteNumbers :: [Integer]
infiniteNumbers = [1..]  -- Alternatively, use enumFrom 1

-- Gets the first n elements from the infinite list
firstN :: Int -> [Integer]
firstN n = take n infiniteNumbers

-- Main function to demonstrate usage
main :: IO ()
main = do
    let n = 10
    putStrLn $ "First " ++ show n ++ " numbers from infinite list:"
    print (firstN n)
```

---

### 🔧 How to Run:

1. Save the code to a file named `InfiniteNumbers.hs`
2. Compile and run using GHC:

```bash
ghc InfiniteNumbers.hs -o infiniteNumbers
./infiniteNumbers
```

Or run in GHCi:

```bash
ghci InfiniteNumbers.hs
*Main> main
First 10 numbers from infinite list:
[1,2,3,4,5,6,7,8,9,10]
```

---

### ✅ Explanation:

* `infiniteNumbers` is a pure infinite list: `[1..]` generates numbers from 1 to infinity.
* `take n` safely extracts the first `n` elements from any infinite list.
* This leverages Haskell’s lazy evaluation.


