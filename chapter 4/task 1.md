```haskell
-- Define weatherReport using pattern matching
weatherReport :: String -> String
weatherReport "sunny"  = "It's a bright and beautiful day!"
weatherReport "rainy"  = "Don't forget your umbrella!"
weatherReport "cloudy" = "A bit gloomy, but no rain yet!"
weatherReport _        = "Weather unknown"

-- Main function to test weatherReport
main :: IO ()
main = do
    putStrLn ("weatherReport \"sunny\" = " ++ weatherReport "sunny")
    putStrLn ("weatherReport \"rainy\" = " ++ weatherReport "rainy")
    putStrLn ("weatherReport \"cloudy\" = " ++ weatherReport "cloudy")
    putStrLn ("weatherReport \"windy\" = " ++ weatherReport "windy")
```

---

### 🔧 How to Run:

1. Save the code in a file named `WeatherReport.hs`
2. Compile using:

   ```bash
   ghc WeatherReport.hs
   ```
3. Run the program:

   ```bash
   ./WeatherReport
   ```

---

### ✅ Expected Output:

```
weatherReport "sunny" = It's a bright and beautiful day!
weatherReport "rainy" = Don't forget your umbrella!
weatherReport "cloudy" = A bit gloomy, but no rain yet!
weatherReport "windy" = Weather unknown
