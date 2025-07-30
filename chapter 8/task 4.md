1. `extractPlayers`: extracts player names from a list of `(name, score)` tuples.
2. `sortByScore`: sorts the list of tuples by score **descending**.
3. `topThree`: returns the top 3 elements of a list.
4. `getTopThreePlayers`: composes the above functions to return the top 3 player names.

---

### ✅ Haskell Code:

```haskell
import Data.List (sortBy)
import Data.Ord (comparing)

-- Type synonym for clarity
type Player = (String, Int)

-- Extract player names from the list
extractPlayers :: [Player] -> [String]
extractPlayers = map fst

-- Sort players by score in descending order
sortByScore :: [Player] -> [Player]
sortByScore = sortBy (flip (comparing snd))

-- Get the top three elements
topThree :: [Player] -> [Player]
topThree = take 3

-- Compose functions to get top three player names
getTopThreePlayers :: [Player] -> [String]
getTopThreePlayers = extractPlayers . topThree . sortByScore

-- Example usage
main :: IO ()
main = do
    let players =
            [ ("Alice", 50)
            , ("Bob", 70)
            , ("Charlie", 60)
            , ("Dave", 80)
            , ("Eve", 40)
            ]
    putStrLn "Top three players:"
    print (getTopThreePlayers players)
```

---

### 💡 Explanation:

* `sortByScore` uses `comparing snd` and `flip` to sort scores in **descending** order.
* `topThree` gets the first 3 from the sorted list.
* `extractPlayers` gets only the names.
* `getTopThreePlayers` composes them:
  `extractPlayers . topThree . sortByScore`

---

### 🧪 Output:

```
Top three players:
["Dave","Bob","Charlie"]
