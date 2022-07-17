## Numbers

### Utilities 
INCR ++number
DECR --number
INCRBY increase by number
DECRBY decrease by number
INCRBYFLOAT increase by float string

### Example
```
SET age 20 GET=> (age: "20")
DECR age=> (age: 19)
INCR age => (age : 20)
DECRBY age 5 => (age: 15)
INCRBY age 6 => (age: 21)
INCRBYFLOAT age 1.11 => (age: "22.11")
```


