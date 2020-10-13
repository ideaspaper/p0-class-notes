[**Back to Home**](./../README.md)

# Pseudocode Note 3

## Function

```javascript
function penambahan(angka1, angka2) {
  let hasil = angka1 + angka2;
  return hasil
}
```

```
BEGIN penambahan
  PASS IN: angka1 AS NUMBER, angka2 AS NUMBER
  STORE hasil AS NUMBER WITH 0
  SET hasil TO angka1 PLUS angka2
  PASS OUT: hasil
END
```

## Array

### Deklarasi

```
// Deklarasi dan assignment array
STORE arr1 WITH [10, 20, 'A', 'B']
STORE arr2 AS ARRAY WITH [10, 20, 'A', 'B']
```

### Looping and Indexing

```
STORE arr WITH [10, 20, 'A', 'B']

FOR i FROM 0 TO (LENGTH OF arr MINUS 1) INCREMENT BY 1
  DISPLAY arr INDEX i
END FOR
```

### Push

```
STORE arr WITH []

PUSH 10 TO arr
PUSH 20 TO arr
PUSH 'A' TO arr
PUSH 'B' TO arr
```

[**Back to Home**](./../README.md)
