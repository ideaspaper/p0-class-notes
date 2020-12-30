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

  // Cari nilai max
  let max = 0;
  for (let i = 0; i < arrIn.length; i++) {
    if (arrIn[i] > max) {
      max = arrIn[i];
    }
  }

  // Cari nilai min
  let min = arrIn[0];
  for (let i = 1; i < arrIn.length; i++) {
    if (arrIn[i] < min) {
      min = arrIn[i];
    }
  }

  if (arrIn.length > 0) {
    return [max, min];
  }
  return [];
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
  let ret = [];
  for (let i = 0; i < str.length; i++) {
    ret.push(str[i]);
  }

  return ret;
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
  let ret = [];

  for (let i = 0; i < input.length; i++) {
    let tidakAda = true;

    for (let j = 0; j < ret.length; j++) {
      if (input[i] === ret[j]) {
        tidakAda = false;
        break;
      }
    }

    if (tidakAda === true) {
      ret.push(input[i]);
    }
  }

  return ret;
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
  let ret = [];

  let retStr = '';
  for (let i = 0; i < str.length; i++) {
    if (str[i] !== sep) {
      retStr += str[i];
    } else if (str[i] === sep) {
      ret.push(retStr);
      retStr = '';
    }
    if (i === str.length - 1) {
      ret.push(retStr);
    }
  }

  return ret;
}

console.log(splitString("2341;3429;864;1309;1276", ";")); // [ '2341', '3429', '864', '1309', '1276' ]
```

[**Back to Home**](./../README.md)