[**Back to Home**](./../README.md)

# 1. Largest Smallest

## Objectives

- Mampu menyelesaikan masalah yang diberikan.
- Mampu mengakses array.
- Mampu membuat dan menggunakan function.

## Directions

Buat sebuah function yang akan mencari nilai terbesar dan nilai terkecil dalam sebuah array. Hasil dari function tersebut berupa array dengan dua element, di mana element pertama merupakan angka terbesar dan element kedua merupakan angka terkecil. Function ini akan menerima 1 parameter:

- `arrIn`: input array.

## Notes

- Jawaban tidak boleh menggunakan built-in function selain `.push()`.

## Implement

```javascript
function maxMin(arrIn) {
  // Do something here
}

console.log(maxMin([5, 1, 7, 12, 2, 8, 5, 6, 1, 12])); // [12, 1]
console.log(maxMin([13])); // [13, 13]
console.log(maxMin([])); // []
```

# 2. Split String to Array

## Objectives

- Mampu menyelesaikan masalah yang diberikan.
- Memahami indexing string dan array.
- Mampu membuat dan mengakses array.
- Mampu membuat dan menggunakan function.

## Directions

Buat sebuah function yang akan memisahkan huruf-huruf yang terdapat pada suatu string ke dalam sebuah array, kemudian me-return array tersebut. Function ini akan menerima satu parameter:

- `str`: string yang hendak diubah menjadi array.

## Notes

- Jawaban tidak boleh menggunakan built-in function selain `.push()`.

## Implement

```javascript
function splitString(str) {
  // Do something here
}

console.log(splitString("Hello")); // ['H', 'e', 'l', 'l', 'o']
```

# 3. Remove Duplicates in Array

## Objectives

- Mampu menyelesaikan masalah yang diberikan.
- Mampu membuat dan mengakses array.
- Mampu membuat dan menggunakan function.

## Directions

Buat sebuah function yang akan menghilangkan nilai duplikat yang terdapat dalam array. Fungsi ini akan menerima satu parameter:

- `input`: input array.

## Notes

- Jawaban tidak boleh menggunakan built-in function selain `.push()`.
- Setiap elemen pada array memiliki tipe number atau string.

## Implement

```javascript
function arrSet(input) {
  // Do something here
}

console.log(arrSet([1, 1, 1, 3, 3, 3, 5, 5, 5, 5])); // [ 1, 3, 5 ]
console.log(arrSet([1, 1, 1, 2, 2, 3, 3, 5, 5])); // [ 1, 2, 3, 5 ]
console.log(arrSet([1, 1, 1, 2, 2, 3, 3, 5, 5, "A", "A"])); // [ 1, 2, 3, 5, 'A' ]
```

# 4. Split String to Array 2

## Objectives

- Mampu menyelesaikan masalah yang diberikan.
- Memahami indexing string dan array.
- Mampu membuat dan mengakses array.
- Mampu membuat dan menggunakan function.

## Directions

Buat sebuah function yang akan menghasilkan sebuah array. Masing-masing elemen dari array tersebut adalah hasil dari memisahkan suatu string berdasarkan penanda tertentu.

- `str`: string yang hendak diubah menjadi array.
- `sep`: karakter yang hendak digunakan sebagai pemisah.

## Notes

- Jawaban tidak boleh menggunakan built-in function selain `.push()`.
- Setiap elemen pada array memiliki tipe number atau string.

## Implement

```javascript
function splitString(str, sep) {
  // Do something here
}

console.log(splitString("2341;3429;864;1309;1276", ";")); // [ '2341', '3429', '864', '1309', '1276' ]
```

[Answers](./array-review-answered.md)

[**Back to Home**](./../README.md)