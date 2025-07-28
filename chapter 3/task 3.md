```haskell
import Text.Printf (printf)

-- Function to convert (R, G, B) to Hex string
rgbToHex :: (Int, Int, Int) -> String
rgbToHex (r, g, b) =
    let rHex = printf "%02X" r
        gHex = printf "%02X" g
        bHex = printf "%02X" b
    in rHex ++ gHex ++ bHex

-- Main function to test rgbToHex
main :: IO ()
main = do
    let color1 = rgbToHex (255, 0, 127)
    let color2 = rgbToHex (0, 255, 64)

    putStrLn ("rgbToHex (255, 0, 127) = " ++ color1)
    putStrLn ("rgbToHex (0, 255, 64) = " ++ color2)
```

---

### 🔧 How to Run:

1. Save the code as `RGBToHex.hs`.
2. Compile it:

   ```bash
   ghc RGBToHex.hs
   ```
3. Run:

   ```bash
   ./RGBToHex
   ```

--
### ✅ Expected Output:

```
rgbToHex (255, 0, 127) = FF007F
rgbToHex (0, 255, 64) = 00FF40
```

---

### 🔍 Notes:

* `printf "%02X"` formats an `Int` to a **2-digit uppercase hexadecimal**.
* `let` bindings are used to define `rHex`, `gHex`, and `bHex` locally before combining them.

