## DEL command
key -> key we are trying to SET

### Example
```
MSET color red color2 green
DEL color 
GET color => null
```