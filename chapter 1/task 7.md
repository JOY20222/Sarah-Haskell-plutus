```haskell
-- Define the conversion function
fToC :: Float -> Float
fToC f = (f - 32) * 5 / 9

-- Main function to test the conversion
main :: IO ()
main = do
    let fahrenheit = 98.6
    let celsius = fToC fahrenheit
    putStrLn ("Temperature in Fahrenheit: " ++ show fahrenheit)
    putStrLn ("Converted to Celsius: " ++ show celsius)
```

### How It Works:

* The formula to convert Fahrenheit to Celsius is:
  $(F - 32) \times \frac{5}{9}$
* `fToC` takes a `Float` as input and returns the corresponding Celsius temperature.

### How to Run:

1. Save it as `FToC.hs`.
2. Compile using GHC:

   ```bash
   ghc FToC.hs
   ```
3. Run the executable:

   ```bash
   ./FToC
   ```

### Example Output:

```
Temperature in Fahrenheit: 98.6
Converted to Celsius: 37.0
```
