```haskell
main :: IO ()
main = do
    putStrLn "Enter something (type 'quit' to exit):"
    loop

loop :: IO ()
loop = do
    input <- getLine
    if input == "quit"
        then putStrLn "Goodbye!"
        else do
            putStrLn ("You entered: " ++ input)
            loop
```

---

### 🧠 Explanation:

* `main` starts the program and calls `loop`.
* `loop` reads input using `getLine`.
* If the input is `"quit"`, it stops and says goodbye.
* Otherwise, it prints the input and calls itself again (`loop`) for the next round.

---

### ✅ Example Run:

```
Enter something (type 'quit' to exit):
hello
You entered: hello
test
You entered: test
quit
Goodbye!
```

---

### ▶️ How to Run:

1. Save as `Main.hs`
2. Compile and run:

   ```bash
   ghc Main.hs -o repeatInput
   ./repeatInput
   ```

Or run in GHCi:

```bash
ghci Main.hs
main
