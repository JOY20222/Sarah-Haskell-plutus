```haskell
-- Define the recursive parametric data type Sequence
data Sequence a = End
                | Node a (Sequence a)
                deriving (Show)

-- Function to check if an element is in the sequence
elemSeq :: Eq a => a -> Sequence a -> Bool
elemSeq _ End = False
elemSeq x (Node y rest)
    | x == y    = True
    | otherwise = elemSeq x rest

-- Example sequence of integers
seq1 :: Sequence Int
seq1 = Node 1 (Node 2 (Node 3 End))

-- Example sequence of strings
seq2 :: Sequence String
seq2 = Node "a" (Node "b" (Node "c" End))

-- Main function to test elemSeq
main :: IO ()
main = do
    print (elemSeq 2 seq1)       -- True
    print (elemSeq 4 seq1)       -- False
    print (elemSeq "b" seq2)     -- True
    print (elemSeq "x" seq2)     -- False
```

---

### 🔍 Explanation

* `elemSeq :: Eq a => a -> Sequence a -> Bool` recursively checks:

  * If the sequence is empty (`End`), return `False`.
  * If the current node's value equals the search value, return `True`.
  * Otherwise, continue checking the rest of the sequence.

---

### ✅ Sample Output

```
True
False
True
False
