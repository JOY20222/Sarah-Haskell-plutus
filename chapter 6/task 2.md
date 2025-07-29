```haskell
-- Recursive Fibonacci function
fibonacci :: Integer -> Integer
fibonacci 0 = 0
fibonacci 1 = 1
fibonacci n = fibonacci (n - 1) + fibonacci (n - 2)

-- Example usage (main function to print the 10th Fibonacci number)
main :: IO ()
main = do
    let n = 10
    putStrLn ("The " ++ show n ++ "th Fibonacci number is: " ++ show (fibonacci n))
```

---

### 📘 Explanation:

#### 🔢 What is the Fibonacci sequence?

The Fibonacci sequence is defined as:

```
fib(0) = 0
fib(1) = 1
fib(n) = fib(n-1) + fib(n-2)   for n > 1
```

#### 🧠 How the recursion works:

The function `fibonacci` is defined recursively:

* If `n` is `0`, it returns `0`
* If `n` is `1`, it returns `1`
* For any `n > 1`, it computes the result by recursively calling `fibonacci (n-1)` and `fibonacci (n-2)` and adding them together.

#### 🔁 Example trace for `fibonacci 5`:

```
fibonacci 5
= fibonacci 4 + fibonacci 3
= (fibonacci 3 + fibonacci 2) + (fibonacci 2 + fibonacci 1)
= ...
```

> Note: This recursive approach is simple but **not efficient** for large `n`, since it recalculates values repeatedly. For better performance, **memoization** or an **iterative version** is preferred.

---

### 🧪 How to run:

1. Save the code in a file named `Fibonacci.hs`
2. Compile it using GHC:

   ```
   ghc Fibonacci.hs
   ```
3. Run the executable:

   ```
   ./Fibonacci
