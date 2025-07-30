```haskell
-- Define the Person type using record syntax
data Person = Person
  { name :: String
  , age :: Int
  , isEmployed :: Bool
  } deriving (Show)

-- Create person1 who is employed
person1 :: Person
person1 = Person
  { name = "Alice"
  , age = 30
  , isEmployed = True
  }

-- Create person2 who is unemployed
person2 :: Person
person2 = Person
  { name = "Bob"
  , age = 25
  , isEmployed = False
  }

-- Example usage
main :: IO ()
main = do
  putStrLn "Person 1:"
  print person1
  putStrLn "Person 2:"
  print person2 
