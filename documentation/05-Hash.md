## Hash

Hash is a collection of key value pairs
Not allowed to have deeply nested object or array

### Commands
- HSET 
- HGET
- HGETALL
- HEXISTS - looking for existence, even falsy value will return in 1
- DEL
- HDEL - delete 1 key value pair

Numbers in Hash
- HINCRBY - same as INCR but for hash but if key does not exist it will be created
- HINCRBYFLOAT - same as INCRBYFLOAT but for hash

String in Hash
- HSTRLEN - get length of string in hash
- HKEYS - get all keys in array
- HVALS - get all values in array

### Example
```
HSET company name company_a revenue 100 
HGET company name => "company_a"
HGETALL company => {name: company_a, revenue: 100} || [name, company_a, revenue, 100]
HEXISTS company age => 1
HEXISTS company people => 0
HDEL company age => delete only age from the hash
DEL company => delete entire hash
HSET company name company_a revenue 100 
HINCRBY company revenue 10 => {name: company_a, revenue: 110}
HINCRBY company age 10 => {name: company_a, revenue: 110, age: 10}
HKEYS company => [name, revenue, age]
HVALS company => [company_a, 110, 10]
```


