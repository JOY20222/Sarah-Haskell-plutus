```haskell
-- Define the recursive Tweet data type
data Tweet = Tweet
    { content  :: String
    , likes    :: Int
    , comments :: [Tweet]
    } deriving (Show)

-- Example tweets with nested comments
comment1 :: Tweet
comment1 = Tweet
    { content = "Nice post!"
    , likes = 5
    , comments = []
    }

comment2 :: Tweet
comment2 = Tweet
    { content = "I disagree"
    , likes = 2
    , comments = []
    }

mainTweet :: Tweet
mainTweet = Tweet
    { content = "Hello, Haskell!"
    , likes = 20
    , comments = [comment1, comment2]
    }

-- Function to display a tweet (with indentation for comments)
displayTweet :: Tweet -> Int -> String
displayTweet (Tweet c l cs) indent =
    replicate indent ' ' ++ "- " ++ c ++ " (" ++ show l ++ " likes)\n" ++
    concatMap (\t -> displayTweet t (indent + 2)) cs

-- Main function
main :: IO ()
main = putStrLn (displayTweet mainTweet 0)
```

---

### 🔍 Explanation

* `Tweet` is a **recursive data type**: each tweet can have other tweets as comments.
* `comments :: [Tweet]` enables nesting.
* `displayTweet` is a recursive function that pretty-prints tweets and their replies using indentation.

---

### ✅ Sample Output

```
- Hello, Haskell! (20 likes)
  - Nice post! (5 likes)
  - I disagree (2 likes)
