```haskell
-- Define the Color data type with Enum and Bounded
data Color = Red | Green | Blue
    deriving (Show, Eq, Enum, Bounded)

-- Define the nextColor function
nextColor :: Color -> Color
nextColor c
    | c == maxBound = minBound
    | otherwise     = succ c

-- Example usage
main :: IO ()
main = do
    print (nextColor Red)    -- Green
    print (nextColor Green)  -- Blue
    print (nextColor Blue)   -- Red (wrap around)
```

---

### 💡 Explanation:

* `deriving (Show, Eq, Enum, Bounded)`:

  * `Enum` allows using `succ` (next) and `pred` (previous),
  * `Bounded` provides `minBound` and `maxBound` for the type.
* `nextColor` checks if the current color is the last (`maxBound`), and if so, wraps around to `minBound`; otherwise, returns the next using `succ`.

---

### 🧪 Output:

```haskell
Green
Blue
Red
```

---

You can compile and run this with:

```bash
ghc NextColor.hs -o nextcolor
./nextcolor
