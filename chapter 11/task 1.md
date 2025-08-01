```haskell
main :: IO ()
main = do
    putStrLn "What is your name?"
    name <- getLine
    putStrLn ("Hello, " ++ name ++ "!")
```

### How it works:

* `main` is the entry point of the program.
* `putStrLn` prints a message to the console.
* `getLine` reads a line of input from the user.
* `name <- getLine` stores the user input in the variable `name`.
* `"Hello, " ++ name ++ "!"` constructs a greeting using string concatenation.

### How to run:



```bash
ghc Main.hs -o greet
./greet
```

Or run it directly in GHCi:

```bash
ghci
:l Main.hs
main
```
