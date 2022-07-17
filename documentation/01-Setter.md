## SET command
key -> key we are trying to SET
value -> Value we want to store

`SET key value`

### Options
* EX seconds -- Set the specified expire time, in seconds.
* PX milliseconds -- Set the specified expire time, in milliseconds.
* EXAT timestamp-seconds -- Set the specified Unix time at which the key will expire, in seconds.
* PXAT timestamp-milliseconds -- Set the specified Unix time at which the key will expire, in milliseconds.
* NX -- Only set the key if it does not already exist.
* XX -- Only set the key if it already exist.
* KEEPTTL -- Retain the time to live associated with the key.
* GET -- Return the old string stored at key, or nil if key did not exist. An error is returned and SET aborted if the value stored at key is not a string.

### Example Basic
```
SET color red  (set color: red)
SET color green GET (set color: green, response: red)
SET asdf 'hello' XX (response: null) 
SET asdf 'hello' NX (set asdf: hello)
SET asdf 'hello 2' XX (set asdf: hello 2)
```

### Example Expiration

```
SET color red EX 2 (set color: red, expires after 2 second)
```

### Type of setter
* SETEX -- Set with EX (may be deprecated depending on your redis)
* SETNX -- Set with NX 
* MSET -- set multiple key value pair

```
SETEX color 2 red => (set color: red, expires in 2 second)
MSET color red secondarycolor green (set color: red, set secondarycolor: green)
SETRANGE color 2 blue => (set color: reblue)
```

