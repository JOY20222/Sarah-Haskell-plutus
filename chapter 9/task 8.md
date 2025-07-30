```haskell
-- Define the recursive parametric data type Sequence
data Sequence a = End                 -- Represents the end of the sequence
                | Node a (Sequence a) -- A node with a value and the rest of the sequence
                deriving (Show)

-- Example sequence of integers: 1 -> 2 -> 3 -> End
seq1 :: Sequence Int
seq1 = Node 1 (Node 2 (Node 3 End))

-- Example sequence of strings: "a" -> "b" -> End
seq2 :: Sequence String
seq2 = Node "a" (Node "b" End)

-- Function to convert Sequence to a standard list for easier viewing
toList :: Sequence a -> [a]
toList End         = []
toList (Node x xs) = x : toList xs

-- Main function to test the sequence
main :: IO ()
main = do
    putStrLn "Sequence of Ints:"
    print (toList seq1)

    putStrLn "Sequence of Strings:"
    print (toList seq2)
```

---

### 🔍 Explanation

* `Sequence a` is a **recursive data structure**:

  * `End` represents the end of the sequence.
  * `Node a (Sequence a)` contains a value and a reference to the next node.
* `toList` is a helper function that converts the custom sequence into a standard Haskell list for easy output.

---

### ✅ Sample Output

```
Sequence of Ints:
[1,2,3]
Sequence of Strings:
["a","b"]
