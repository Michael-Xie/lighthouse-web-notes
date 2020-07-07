# Week 1

- `lein repl`
- examples of clojure functions
	- (+ 1 2 3 4) which adds the numbers
	- (first [1 2 3 4]) which takes the first number of the array
- *prefix notation* syntax, which means operator comes first in an expression

## Forms
- valid code
- aka expression

- two structures
	- literal rep of data structs like num, str, maps, and vectors
- operations

```
(operator operand1 operand2 ... operandn)
```

## Control Flow

### if
```
(if boolean-form
  then-form
  optional-else-form)
```
### or
- wrap multiple forms in paren
- used with if because if only can take one form for if and then cases

### when
when is like if and or but no else branch
```
(when true
	(println "Success!")
	"abra cadabra")
```

## truthiness and falsiness
- `nil` indicates no value
- falsy = nil, false
- named function `nil?`

## or
- returns the first truthy value or last value
## and 
- returns first falsey value or if no falsey then last truthy value
## =
equality

## def
bind name to a value
- treat like defining constants
## defn
create a function

## Data Structures
### Strings
- only double quotes
- no string interpolation, can only concat with `str`

### maps
- similar to dict and hash
- literal
	- {:key value :key2 value}
- `hash-map` function
	- (hash-map :a 1 :b2)
### lookup with `get` function
- (get {:a 1 :b 1} :b) ==> 1
- can return nil or default value, optional param after search key
- `get-in` let s' you look up values in nested maps
- can lookup like a funciton with key as arg
```
({:name "The Human Coffeepot"} :name)
; => "The Human Coffeepot"
```

## keywords
- examples: :a, :34
- can be used as functions to lookup corresponding data struct
```
(:a {:a 1 :b 2 :c 3})
=> 1
```


## Vectors
- similar to array
- look up is like maps
- [3 2 1]
- or with vector function
```
(vector "creepy" "full" "moon")
=> ["creepy" "full" "moon"]
- add with `conj` function
```
(conj [1 2 3] 4)
=> [1 2 3 4]
```

## Lists
- literal `'(1 2 3 4) => (1 2 3 4)`
- can not retrieve element with `get`
- use `nth` function to get
```
(nth `(:a :b :c) 0) => :a
```
- slower than `get` vs `nth`
- can use `list` function to create list
```
(list 1 "two" {3 4})
=> (1 "two" {3 4})
```
- can use `conj` to add to list, but it is added to the front

## Sets
- collection of unique values
- hash sets and sorted sets
- focus on prior

```
#{"kurt vonnegut" 20 :icicle}

(hash-set 1 1 2 2)
=> #{1 2}
```

- conj to add
- and use function `set` for existing vectors
```
(set [3 3 3 4 4])
=> #{3 4}
```

- check for membership with `contains?` function
```
(contains? #{:a :b} :a)
=> true
(:a #{:a :b})
=> true
```

## Functions

### Calling Functions
- aka function expression

- higher order functions = functions that take other functions as arg or return a function

