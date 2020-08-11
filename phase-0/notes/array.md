[**Back to Home**](./../README.md)

# Array

## Apa itu Array?

Array merupakan struktur data (_data structure_), yang artinya, kita dapat menggunakan array sebagai salah satu cara untuk menjadikan data kita menjadi lebih terstruktur. Sebuah array terdiri dari kumpulan elemen-elemen (biasanya sejenis) seperti di bawah.

🍎️ 🥝️ 🍊️ 🍌️ 🍇️ 🥑️   -->   Fruits

🤡️ 🤡️ 🤡️ 🤡️ 🤡️ 🤡️   -->   Clowns

💉️ 💉️ 💉️ 💉️ 💉️ 💉️   -->   Medicines

👧️ 👨‍💼️ 👵️ 👨‍🌾️ 👨‍💻️ 👩‍🏫️   -->   People

Best practice: nama dari sebuah array selalu dalam bentuk jamak (plural).

## Mengapa kita membutuhkan Array?

Amati kode program di bawah ini.

```javascript
function eat(fruit) {
  // Do the eating
}

let apple = 'apple';
let orange = 'orange';
let grape = 'grape';

// Eat them all
eat(apple);
eat(orange);
eat(grape);
```

Pada kode program tersebut, kita memiliki 3 buah data yaitu `'apple'`, `'orange'` dan '`grape'`. Dari pada kita menyediakan sebuah variable untuk masing-masing data, kita dapat memasukkan data-data tersebut ke dalam sebuah array `fruits` saja. Dengan demikian data kita akan menjadi lebih terstruktur seperti kode program di bawah.

```javascript
function eat(fruit) {
  // Do the eating
}

let fruits = ['apple', 'orange', 'grape'];

eat(fruits[0]);
eat(fruits[1]);
eat(fruits[2]);
```

## Pengaksesan elemen Array

Sama seperti string, Array memiliki properti `.length` yang nilainya adalah banyak elemen yang ada di dalam array.

Sama seperti string, elemen Array dapat diakses dengan cara indexing, yang dimulai dari 0.

## Menambahkan elemen ke Array

`.unshift()`

```javascript
let array1 = [1, 2, 3];
array1.unshift(4);
console.log(array1); // [4, 1, 2, 3]
```

`.push()`

```javascript
let array1 = [1, 2, 3];
array1.push(4);
console.log(array1); // [1, 2, 3, 4]
```

## Menghapus elemen Array

`.shift()`

```javascript
let array1 = [1, 2, 3];
let firstElement = array1.shift();
console.log(array1); // [2, 3]
console.log(firstElement); // 1
```

`.pop()`

```javascript
let array1 = [1, 2, 3];
let lastElement = array1.pop();
console.log(array1); // [1, 2]
console.log(lastElement); // 3
```

## Memeriksa apakah array itu kosong

Sebuah Array dimungkinkan untuk tidak memiliki elemen sama sekali. Kita tidak dapat melakukan pengecekan sebuah Array kosong seperti di bawah ini.

```javascript
let array1 = [];
if (array1 === []) {
  console.log('This is an empty array');
} else {
  console.log('This is not an empty array');
}
```

Alasannya karena Array adalah sebuah Object pada JavaScript. Materi mengenai Object akan diberikan pada lecture yang akan datang.

Pengecekan Array kosong dapat dilakukan dengan memanfaatkan properti `.length`.

```javascript
let array1 = [];
if (array1.length === 0) {
  console.log('This is an empty array');
} else {
  console.log('This is not an empty array');
}
```

## Array vs String

Array dan string memiliki kesamaan, yaitu memiliki properti `.length` dan dapat diakses menggunakan indexing.

Perbedaannya adalah string bersifat **immutable** (nilainya tidak dapat diubah), sedangkan array bersifat **mutable** (nilainya dapat diubah). Coba jalankan dan amati hasil dari kode program di bawah.

```javascript
let string1 = 'Oskadon';
string1[0] = 'A';
console.log(string1);

let array1 = ['O', 's', 'k', 'a', 'd', 'o', 'n'];
array1[0] = 'A';
console.log(array1);
```

Selain itu, tidak terdapat built-in function `.unshift()`, `.push()`, `.shift()` dan `.pop()` pada string.

## Latihan 1

```javascript
/**
 * Buatlah program untuk mensimulasikan pembacaan suhu sebuah ruangan sebanyak times.
 * Pembacaan suhu memiliki rentang dari 1 - 100.
 * Tampung hasil-hasil pembacaan suhu tersebut ke dalam sebuah array.
 */

let times = 10;
let tempReadings = [];

// Code here
```

## Latihan 2

```javascript
/**
 * Terdapat sebuah array of string 'fruits' yang berisi nama buah-buahan.
 * Buatlah sebuah program yang akan:
 *   1. Menampilkan semua nama buah ke bawah pada terminal
 *   2. Menampilkan nama buah dengan index genap ke bawah pada terminal
 *   3. Menampilkan nama buah dengan length lebih dari 5
 *   4. Menampilkan nama buah yang memiliki awalan huruf 'M'
 *   5. Mengubah nama buah dengan index ganjil menjadi nilai dari index tersebut
 */

let fruits = ['Orange', 'Apple', 'Mango', 'Banana', 'Watermelon', 'Melon', 'Pear'];

// Code here
```

[Answers](./array-answered.md)

[**Back to Home**](./../README.md)
