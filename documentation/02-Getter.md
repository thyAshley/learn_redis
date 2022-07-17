## GET command
key -> key we are trying to SET

### Example
```
MSET color red color2 green
GET color => (response: "red")
MGET color color2 => (response: ["red", "green"])
```

GETRANGE
```
MSET color red color2 green
GETRANGE color 0 1 => "re"
```

