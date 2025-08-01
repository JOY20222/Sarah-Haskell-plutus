```haskell
main :: IO ()
main = do
    putStrLn "Please choose an option:"
    putStrLn "1. Greet"
    putStrLn "2. Show a fun fact"
    putStrLn "3. Exit"
    putStrLn "Enter your choice (1, 2, or 3):"
    choice <- getLine
    handleChoice choice

handleChoice :: String -> IO ()
handleChoice choice =
    case choice of
        "1" -> do
            putStrLn "What is your name?"
            name <- getLine
            putStrLn ("Hello, " ++ name ++ "!")
        "2" -> putStrLn "Fun Fact: Haskell is a purely functional programming language named after Haskell Curry."
        "3" -> putStrLn "Goodbye!"
        _   -> do
            putStrLn "Invalid option. Please enter 1, 2, or 3."
            main  -- restart the menu
```

---

### 🧠 Explanation:

* The menu is printed with three options.
* The user enters a choice (`getLine`).
* `handleChoice` uses a `case` expression to match the input and perform the appropriate action.
* If the input is invalid, the program restarts by calling `main` again.

---

### ✅ Example Run:

```
Please choose an option:
1. Greet
2. Show a fun fact
3. Exit
Enter your choice (1, 2, or 3):
1
What is your name?
Sarah
Hello, Sarah!
```

---

### ▶️ How to Run:

1. Save as `Main.hs`
2. Compile:

   ```bash
   ghc Main.hs -o menuProgram
   ./menuProgram
   ```

Or run in GHCi:

```bash
ghci Main.hs
main
