```haskell
-- Define the Book type with Show deriving
data Book = Book
  { title  :: String
  , author :: String
  , year   :: Int
  } deriving (Show)

-- Create an instance of Book
myBook :: Book
myBook = Book
  { title = "The Haskell Road to Logic, Math and Programming"
  , author = "Kees Doets and Jan van Eijck"
  , year = 2004
  }

-- Main function to print the book
main :: IO ()
main = do
  putStrLn "Book information:"
  print myBook
```

---

### 💡 Explanation:

* `data Book = Book { ... } deriving (Show)` automatically creates a readable `String` representation of the book.
* The `print` function uses that derived `Show` instance to display the `Book`.

---

### 🧪 Sample Output:

```
Book information:
Book {title = "The Haskell Road to Logic, Math and Programming", author = "Kees Doets and Jan van Eijck", year = 2004}
