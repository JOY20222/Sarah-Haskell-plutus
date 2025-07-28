```haskell
-- Define gradeComment using guards
gradeComment :: Int -> String
gradeComment grade
    | grade >= 90 && grade <= 100 = "Excellent!"
    | grade >= 70 && grade <= 89  = "Good job!"
    | grade >= 50 && grade <= 69  = "You passed."
    | grade >= 0 && grade <= 49   = "Better luck next time."
    | otherwise                   = "Invalid grade"

-- Main function to test gradeComment
main :: IO ()
main = do
    putStrLn ("gradeComment 95 = " ++ gradeComment 95)
    putStrLn ("gradeComment 75 = " ++ gradeComment 75)
    putStrLn ("gradeComment 60 = " ++ gradeComment 60)
    putStrLn ("gradeComment 40 = " ++ gradeComment 40)
    putStrLn ("gradeComment (-5) = " ++ gradeComment (-5))
    putStrLn ("gradeComment 105 = " ++ gradeComment 105)
```

---

### 🔧 How to Run:

1. Save the code in a file named `GradeComment.hs`
2. Compile with:

   ```bash
   ghc GradeComment.hs
   ```
3. Run the program:

   ```bash
   ./GradeComment
   ```

---

### ✅ Expected Output:

```
gradeComment 95 = Excellent!
gradeComment 75 = Good job!
gradeComment 60 = You passed.
gradeComment 40 = Better luck next time.
gradeComment (-5) = Invalid grade
gradeComment 105 = Invalid grade
