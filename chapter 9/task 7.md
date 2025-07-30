```haskell
-- Define the recursive Tweet data type
data Tweet = Tweet
    { content  :: String
    , likes    :: Int
    , comments :: [Tweet]
    } deriving (Show)

-- Example tweets
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

nestedComment :: Tweet
nestedComment = Tweet
    { content = "Reply to disagreement"
    , likes = 3
    , comments = []
    }

comment2WithReply :: Tweet
comment2WithReply = comment2 { comments = [nestedComment] }

mainTweet :: Tweet
mainTweet = Tweet
    { content = "Hello, Haskell!"
    , likes = 20
    , comments = [comment1, comment2WithReply]
    }

-- Function to calculate total engagement recursively
engagement :: Tweet -> Int
engagement (Tweet _ l cs) = l + sum (map engagement cs)

-- Main function to test engagement
main :: IO ()
main = do
    putStrLn ("Engagement: " ++ show (engagement mainTweet))
```

---

### 🔍 Explanation

* `engagement :: Tweet -> Int`: recursively adds the likes of the tweet and all nested comment tweets.
* Uses `map engagement cs` to recursively apply the function to each comment in the list.

---

### ✅ Sample Output

```
Engagement: 30
```

> (20 from main tweet, 5 from `comment1`, 2 from `comment2`, 3 from `nestedComment`)
