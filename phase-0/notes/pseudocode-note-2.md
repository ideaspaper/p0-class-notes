[**Back to Home**](./../README.md)

# Pseudocode Note 2

## Switch-Case

```
SWITCH namaVariable
  CASE nilai1
    ...
  CASE nilai2
    ...
  CASE nilai3
    ...
END SWITCH
```

## For Loop

```
FOR i FROM 0 TO 9 INCREMENT BY 1
  DISPLAY 'Hello'
END FOR
```

## While Loop

```
STORE i WITH 0
WHILE i LESS THAN 10
  DISPLAY 'Hello'
  SET i WITH i PLUS 1
END WHILE
```

## Do-While Loop

```
STORE i WITH 0
DO
  DISPLAY 'Hello'
  SET i WITH i PLUS 1
WHILE i LESS THAN 10
```

## Break

```
STORE i WITH 1

WHILE i LESS THAN 100
  DISPLAY i
  IF i MODULUS BY 25 EQUAL 0
    DISPLAY 'Kelipatan 25 sudah ketemu'
    BREAK
  END IF
  SET i TO i PLUS 1
END WHILE
```

## Length and Indexing

```
STORE input WITH 'Nama saya Acong'

// Menampilkan panjang dari input
DISPLAY LENGTH OF input

// Mengakses huruf pertama pada input
DISPLAY input[0]

// Mengakses huruf terakhir pada input
DISPLAY input[LENGTH OF input]

// Mengakses huruf ke-n pada input
DISPLAY input[1] // Huruf ke 2
DISPLAY input[2] // Huruf ke 3
```

## Built-in Function

```
// Contoh Math.random
SET variableName WITH RANDOM NUMBER BETWEEN 0 AND 10

// Contoh Math.round
SET variableName WITH ROUND OF variableName

// Contoh Math.floor
SET variableName WITH ROUND DOWN OF variableName

// Contoh Math.ceil
SET variableName WITH ROUND UP OF variableName
```

Penulisan built-in function lainnya yang tidak disebutkan, bisa meniru gaya penulisan di atas.

[**Back to Home**](./../README.md)
