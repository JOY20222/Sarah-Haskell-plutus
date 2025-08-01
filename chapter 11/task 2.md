```haskell
main :: IO ()
main = do
    putStrLn "Enter a line of text:"
    line <- getLine
    let charCount = length line
    putStrLn ("The number of characters is: " ++ show charCount)
```

### Explanation:

* `putStrLn` prints a message prompting the user.
* `getLine` reads a line from the user and stores it in `line`.
* `length line` calculates the number of characters.
* `show` converts the integer result to a string for printing.
* `++` is used to concatenate strings.

### Example:

If the user types:

```
Hello world!
```

The program will output:

```
The number of characters is: 12
```

### Running the program:

1. Save it as `Main.hs`
2. Compile and run it:

   ```bash
   ghc Main.hs -o countChars
   ./countChars
   ```

Or, load and run it in GHCi:

```bash
ghci Main.hs
main
```
