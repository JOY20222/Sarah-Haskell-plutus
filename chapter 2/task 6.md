```haskell
-- Define smallNumber as Int
smallNumber :: Int
smallNumber = 262

-- Define bigNumber as Integer
bigNumber :: Integer
bigNumber = 2127

-- Attempt to compute 2^64 using Int and Integer
main :: IO ()
main = do
    putStrLn ("smallNumber (Int) = " ++ show smallNumber)
    putStrLn ("bigNumber (Integer) = " ++ show bigNumber)

    -- Evaluate 2^64 as Int (may overflow depending on platform)
    let powerInt :: Int
        powerInt = 2 ^ 64

    putStrLn ("2^64 :: Int = " ++ show powerInt)

    -- Evaluate 2^64 as Integer (safe)
    let powerInteger :: Integer
        powerInteger = 2 ^ 64

    putStrLn ("2^64 :: Integer = " ++ show powerInteger)
```

---

### 🔧 How to Run:

1. Save as `BigIntTest.hs`.
2. Compile:

   ```bash
   ghc BigIntTest.hs
   ```
3. Run:

   ```bash
   ./BigIntTest
   ```

---

### ⚠️ Notes on `2^64 :: Int`:

* On **most 64-bit systems**, `Int` is **bounded** to `[-9223372036854775808 .. 9223372036854775807]`.
* `2^64 = 18446744073709551616` is **too large for `Int`**, so it **overflows**, producing an incorrect (and often negative) result.

---

### ✅ Sample Output on a 64-bit System:

```
smallNumber (Int) = 262
bigNumber (Integer) = 2127
2^64 :: Int = 0          -- or another overflowed result
2^64 :: Integer = 18446744073709551616
```
