1. Defines a new type `Employee` using **record syntax** with:

   * `name :: String`
   * `experienceInYears :: Float`
2. Creates an `Employee` named `richard` with **7.5 years of experience**.

---

### ✅ Haskell Code:

```haskell
-- Define the Employee type using record syntax
data Employee = Employee
    { name :: String
    , experienceInYears :: Float
    } deriving (Show)

-- Create an employee named richard
richard :: Employee
richard = Employee
    { name = "Richard"
    , experienceInYears = 7.5
    }

-- Example usage
main :: IO ()
main = do
    putStrLn "Employee details:"
    print richard
```

---

### 💡 Explanation:

* The `Employee` type uses **record syntax** for easy access to fields by name (`name richard`, `experienceInYears richard`).
* `deriving (Show)` allows printing the record in the console.
* `richard` is an instance of `Employee` with specific values.

---

### 🧪 Sample Output:

```
Employee details:
Employee {name = "Richard", experienceInYears = 7.5}
