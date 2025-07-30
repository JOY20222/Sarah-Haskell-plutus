1. Defines a new **algebraic data type** `Animal` with constructors:

   * `Dog String` — where the `String` represents the dog's name
   * `Cat String` — where the `String` represents the cat's name
2. Implements the function `describeAnimal :: Animal -> String` that returns a description of the animal.
3. Creates instances of `Animal`: one dog and one cat.

---

### ✅ Haskell Code

```haskell
-- Define the Animal type with Dog and Cat constructors
data Animal = Dog String | Cat String
  deriving (Show)

-- Function to describe the animal
describeAnimal :: Animal -> String
describeAnimal (Dog name) = "This is a dog named " ++ name ++ "."
describeAnimal (Cat name) = "This is a cat named " ++ name ++ "."

-- Instances of Animal
myDog :: Animal
myDog = Dog "Buddy"

myCat :: Animal
myCat = Cat "Whiskers"

-- Example usage
main :: IO ()
main = do
  putStrLn (describeAnimal myDog)  -- "This is a dog named Buddy."
  putStrLn (describeAnimal myCat)  -- "This is a cat named Whiskers."
```

---

### 💡 Explanation

* `data Animal = Dog String | Cat String` defines a **sum type** with two constructors:

  * `Dog` and `Cat`, each holding a `String` (e.g. a name).
* `describeAnimal` uses **pattern matching** to check if the input is a `Dog` or a `Cat`, and returns a custom description.
* `myDog` and `myCat` are **values of type `Animal`**, using the respective constructors.

---

### 🧪 Sample Output

```
This is a dog named Buddy.
This is a cat named Whiskers.
