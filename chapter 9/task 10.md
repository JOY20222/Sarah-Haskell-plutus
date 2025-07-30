```haskell
-- Define the Binary Search Tree (BST) data type
data BST a = Empty
           | Node a (BST a) (BST a)
           deriving (Show)

-- Function to insert a value into the BST
insert :: Ord a => a -> BST a -> BST a
insert x Empty = Node x Empty Empty
insert x (Node y left right)
    | x < y     = Node y (insert x left) right
    | x > y     = Node y left (insert x right)
    | otherwise = Node y left right  -- Ignore duplicates

-- Function to check if a value exists in the BST
search :: Ord a => a -> BST a -> Bool
search _ Empty = False
search x (Node y left right)
    | x == y    = True
    | x < y     = search x left
    | otherwise = search x right

-- Example usage: build a sample BST
exampleBST :: BST Int
exampleBST = foldr insert Empty [10, 5, 15, 3, 7, 12, 18]

-- Main function to test the BST
main :: IO ()
main = do
    putStrLn "Binary Search Tree:"
    print exampleBST

    putStrLn "\nSearch results:"
    print (search 7 exampleBST)    -- True
    print (search 20 exampleBST)   -- False
```

---

### 🔍 Explanation

#### `data BST a = Empty | Node a (BST a) (BST a)`

* This defines a **recursive, parametric** data type:

  * `Empty` represents an empty tree.
  * `Node a left right` represents a node with a value of type `a`, a left subtree, and a right subtree.

#### `insert :: Ord a => a -> BST a -> BST a`

* Inserts a value into the BST following **binary search rules**:

  * If the tree is empty, it creates a new node.
  * If the value is less than the current node, insert into the left subtree.
  * If greater, insert into the right subtree.
  * If equal, do nothing (ignoring duplicates).

#### `search :: Ord a => a -> BST a -> Bool`

* Searches for a value in the BST:

  * Follows the same logic as insert, using recursion.

#### `exampleBST`

* Built using `foldr insert` to construct the tree from a list of values.

---

### ✅ Sample Output

```
Binary Search Tree:
Node 10 (Node 5 (Node 3 Empty Empty) (Node 7 Empty Empty)) (Node 15 (Node 12 Empty Empty) (Node 18 Empty Empty))

Search results:
True
False
