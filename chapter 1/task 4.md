HC1T4 - Task 4: Composing a Function to Process Player Data

* `extractPlayers` – extracts player names
* `sortByScore` – sorts by score (descending)
* `topThree` – returns top three players
* `getTopThreePlayers` – composed function that performs all steps

---

### ✅ Full Haskell Code

```haskell
-- File: TopThreePlayers.hs

import Data.List (sortBy)
import Data.Ord (comparing)

-- Extracts the player names from a list of (name, score) tuples
extractPlayers :: [(String, Int)] -> [String]
extractPlayers players = map fst players

-- Sorts the list by score in descending order
sortByScore :: [(String, Int)] -> [(String, Int)]
sortByScore = sortBy (flip (comparing snd))

-- Takes the top three players from the sorted list
topThree :: [(String, Int)] -> [(String, Int)]
topThree = take 3

-- Composes the above three functions
getTopThreePlayers :: [(String, Int)] -> [String]
getTopThreePlayers = extractPlayers . topThree . sortByScore

-- Example usage
main :: IO ()
main = do
    let players = [("Alice", 50), ("Bob", 80), ("Charlie", 70), ("Diana", 90), ("Eve", 65)]
    let topPlayers = getTopThreePlayers players
    putStrLn "Top three players:"
    mapM_ putStrLn topPlayers
```

---

### 🔧 How to Run:

1. Save as `TopThreePlayers.hs`
2. Compile and run:

```bash
ghc TopThreePlayers.hs -o topplayers
./topplayers
```

Or run in GHCi:

```bash
ghci TopThreePlayers.hs
*Main> main
Top three players:
Diana
Bob
Charlie
```

---

### ✅ Summary:

* Fully pure and reusable functions.
* `getTopThreePlayers` is a clean composition.
* `map fst`, `sortBy`, and `take` are standard Haskell tools.
* No external state or side effects inside core logic.


