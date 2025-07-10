HC1T1 - Task 1: Function Composition

1. **`double`**: Multiplies a number by 2.
2. **`increment`**: Increases a number by 1.
3. **`doubleThenIncrement`**: Uses function composition to apply `double` first and then `increment`.

```haskell
-- Function to double a number
double :: Int -> Int
double x = x * 2

-- Function to increment a number
increment :: Int -> Int
increment x = x + 1

-- Function to apply double first, then increment (function composition)
doubleThenIncrement :: Int -> Int
doubleThenIncrement = increment . double

-- Main function to test the behavior
main :: IO ()
main = do
    let number = 5
    -- Apply double, then increment
    print ("Double of " ++ show number ++ ": " ++ show (double number))
    print ("Increment of " ++ show number ++ ": " ++ show (increment number))
    print ("Double then Increment of " ++ show number ++ ": " ++ show (doubleThenIncrement number))
```

### Explanation:

* **`double`** multiplies a given integer by 2.
* **`increment`** adds 1 to the given integer.
* **`doubleThenIncrement`** is the composition of `double` and `increment`. Using the composition operator (`.`), `double` is applied first, and then `increment` is applied to the result of `double`.

### Example Output (if `number = 5`):

```text
Double of 5: 10
Increment of 5: 6
Double then Increment of 5: 11
```

In this example, the function `doubleThenIncrement 5` performs:

1. First doubles the number: `5 * 2 = 10`
2. Then increments the result: `10 + 1 = 11`


