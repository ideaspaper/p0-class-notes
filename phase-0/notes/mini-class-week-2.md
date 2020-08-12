[**Back to Home**](./../README.md)

# Strings

String merupakan salah satu tipe data primitive pada JavaScript. Sebuah string akan berisi kumpulan karakter seperti di bawah.

```javascript
let str1 = "Ini adalah sebuah string";
let str2 = "0123456789";
let str3 = "Variable str3 merupakan string";
let str4 = "Meskipun isi str3 adalah angka, angka-angka tersebut adalah karakter, bukan number";
```

Kita dapat melakukan operasi penambahan pada string. Operasi penambahan biasanya dilakukan untuk menggabungkan dua buah string (concatenation). Hasil dari operasi penambahan adalah sebuah string.

```javascript
let str1 = "abc";
let str2 = "def";
let arrNum = [1, 2, 3];
let arrStr = ["1", "2", "3"];

let result1 = str1 + str2;
let result2 = str1 + arrNum;
let result3 = str1 + arrStr;

console.log(result1, typeof result1);
console.log(result2, typeof result2);
console.log(result3, typeof result3);
```

**Tips**: Jika tidak yakin dengan hasil penambahan string, cobalah dengan `console.log()`.

Bagaimana dengan operasi yang lainnya, seperti pengurangan, perkalian, pembagian, dll.?

> Silahkan melakukan eksperimen mandiri dengan `console.log()`.

## String Literals

Bagaimana cara menggabungkan dua buah string? Kita dapat menggunakan operator `+`.

```javascript
let str1 = "Hobi";
let str2 = "Budi";
let str3 = "adalah";
let str4 = "coding";
let str5 = "meskipun umurnya baru";
let num = 12;
let str6 = "tahun";

// Hasilkan output: Hobi Budi adalah coding meskipun umurnya baru 12 tahun
console.log(str1 + " " + str2 + " " + str3 + " " + str4 + " " + str5 + " " + num + " " + str6);
```

Apabila variable yang hendak ditampilkan semakin banyak, maka cara penulisan kode program di atas akan menjadi membingungkan. Maka dari itu kita dapat memanfaatkan string literal. String literal dapat dibuat menggunakan backtick (`). Kode program di atas dapat dituliskan menjadi seperti di bawah.

```javascript
let str1 = "Hobi";
let str2 = "Budi";
let str3 = "adalah";
let str4 = "coding";
let str5 = "meskipun umurnya baru";
let num = 12;
let str6 = "tahun";

// Hasilkan output: Hobi Budi adalah coding meskipun umurnya baru 12 tahun
console.log(`${str1} ${str2} ${str3} ${str4} ${str5} ${num} ${str6}`);
```

## Length dan Indexing

Kita dapat mengetahui panjang suatu string dengan menggunakan properti `.length`. Hasil dari mengakses properti tersebut adalah **PANJANG** dari string.

```javascript
let str = "abcdefghij";
console.log(str.length); // 10
```

Kita dapat mengakses karakter pada sebuah string dengan indexing. Indexing dapat dilakukan dengan menggunakan kurung siku (square bracket). **INDEXING DIMULAI DARI 0**.

```javascript
let str = "abcdefghij";
console.log(str[0]); // a
console.log(str[1]); // b
console.log(str[2]); // c
console.log(str[3]); // d
console.log(str[4]); // e
```

## Immutability

Kita tidak dapat melakukan assignment pada sebuah karakter di dalam string. Hal tersebut dinamakan sebagai sifat immutable (tidak dapat diubah).

```javascript
let str = "Makan soto Makasar";
console.log(str); // Makan soto Makasar
str[6] = "c";
console.log(str); // Makan soto Makasar
```

> Apabila ada soal yang meminta kita mengubah karakter pada string, maka kita harus membuat **STRING BARU**.

# Array

Array merupakan salah satu tipe struktur data. Kegunaan dari array adalah untuk membuat kumpulan data kita menjadi terstruktur. Sebuah array terdiri dari kumpulan elemen-elemen (biasanya sejenis) seperti di bawah.

🍎️ 🥝️ 🍊️ 🍌️ 🍇️ 🥑️ --> Fruits

🤡️ 🤡️ 🤡️ 🤡️ 🤡️ 🤡️ --> Clowns

💉️ 💉️ 💉️ 💉️ 💉️ 💉️ --> Medicines

👧️ 👨‍💼️ 👵️ 👨‍🌾️ 👨‍💻️ 👩‍🏫️ --> People

> Best practice: nama dari sebuah array selalu dalam bentuk jamak (plural).

Array dapat dianalogikan sebagai sebuah rak. Sebagai contoh rak bumbu dapur seperti di bawah.

| Slot 0  | Slot 1 | Slot 2 | Slot3    |
| ------- | ------ | ------ | -------- |
| 'Garam' | 'Cabe' | 'Gula' | 'Terasi' |

## Mengapa kita membutuhkan Array?

Amati kode program di bawah ini.

```javascript
function eat(fruit) {
  // Do the eating
}

let apple = "apple";
let orange = "orange";
let grape = "grape";

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

let fruits = ["apple", "orange", "grape"];

eat(fruits[0]);
eat(fruits[1]);
eat(fruits[2]);
```

## Length dan Indexing

Kita dapat mengetahui panjang suatu array dengan menggunakan properti `.length`. Hasil dari mengakses properti tersebut adalah **BANYAK ELEMEN** dari sebuah array.

```javascript
let arr = ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j"];
console.log(arr.length); // 10
```

Kita dapat mengakses karakter pada sebuah array dengan indexing. Indexing dapat dilakukan dengan menggunakan kurung siku (square bracket). **INDEXING DIMULAI DARI 0**.

```javascript
let arr = ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j"];
console.log(arr[0]); // a
console.log(arr[1]); // b
console.log(arr[2]); // c
console.log(arr[3]); // d
console.log(arr[4]); // e
```

## Mutability

Jika string memiliki sifat immutable, maka array memiliki sifat mutable (nilai suatu elemen array dapat diubah).

```javascript
let arr = ["S", "o", "t", "o"];
console.log(arr); // ["S", "o", "t", "o"]
arr[0] = "C";
console.log(arr); // ["C", "o", "t", "o"]
```

## Menambahkan Elemen ke Array

Kita **TIDAK DAPAT** menambahkan elemen ke array dengan operator `+` seperti pada string. Penambahan elemen ke array dapat dilakukan menggunakan dua buah built-in function berikut.

`.unshift()`

```javascript
let arr = [1, 2, 3];
arr.unshift(4);
console.log(arr); // [4, 1, 2, 3]
```

`.push()`

```javascript
let arr = [1, 2, 3];
arr.push(4);
console.log(arr); // [1, 2, 3, 4]
```

## Menghapus Elemen Array

Pada string kita tidak dapat melakukan pengurangan dengan tujuan untuk menghapus suatu karakter. Hal tersebut dikarenakan sifat immutability dari string. Lain halnya dengan array. Karena array bersifat mutable, kita dapat menghapus elemennya. Penghapusan suatu elemen pada array dapat dilakukan dengan menggunakan dua buah built-in function berikut.

`.shift()`

```javascript
let arr = [1, 2, 3];
let firstElement = arr.shift();
console.log(arr); // [2, 3]
console.log(firstElement); // 1
```

`.pop()`

```javascript
let arr = [1, 2, 3];
let lastElement = arr.pop();
console.log(arr); // [1, 2]
console.log(lastElement); // 3
```

## Memeriksa apakah Array Kosong

Sebuah array dimungkinkan untuk tidak memiliki elemen sama sekali. Kita tidak dapat melakukan pengecekan sebuah array kosong seperti di bawah ini.

```javascript
let arr = [];
if (arr === []) {
  console.log("This is an empty array");
} else {
  console.log("This is not an empty array");
}
```

Alasannya karena array adalah sebuah Object pada JavaScript. Materi mengenai Object akan diberikan pada lecture yang akan datang.

Pengecekan array kosong dapat dilakukan dengan memanfaatkan properti `.length`.

```javascript
let arr = [];
if (arr.length === 0) {
  console.log("This is an empty array");
} else {
  console.log("This is not an empty array");
}
```

# Looping

Looping merupakan pengulangan. Alasan dari penggunaan looping dapat diilustrasikan dengan kode program di bawah.

```javascript
// Cetak "Hello" pada terminal sebanyak 117 kali
console.log("Hello"); // line 1
console.log("Hello"); // line 2
console.log("Hello"); // line 3
        ·
        ·
        ·
console.log("Hello"); // line 117
```

Kode program di atas rawan untuk error dengan alasan sebagai berikut:
- Kita harus benar-benar memperhatikan bahwa ada tepat 117 `console.log("Hello")`.
- Apabila requirement berubah menjadi 275 kali, maka kita harus melakukan _copy-paste_ dengan teliti hingga benar-benar ada 275 line `console.log("Hello")`.

Maka dari itu, bahasa pemrograman pada umumnya menyediakan fitur looping. Pada JavaScript terdapat tiga jenis looping, yaitu `for`, `while` dan `do...while`.

> DRY (Don't Repeat Yourself). Pekerjaan manual yang sama dan dilakukan berkali-kali akan memperbesar kemungkinan terjadinya human error.

## for

Syntax `for` memiliki empat bagian:
1. Inisialisasi
2. Kondisional
3. Increment/decrement
4. Kode program yang dieksekusi

```javascript
// for (inisialisasi; kondisional; increment/decrement) {
//   kode program yang dieksekusi
// }

for (let i = 0; i < 10; i++) {
  console.log("Hello");
}
```

Apabila diterjemahkan ke Bahasa Indonesia, `for` adalah **LAKUKAN X SEBANYAK Y KALI**. Dengan pengertian tersebut, maka `for` tepat untuk digunakan pada pengulangan yang kita tahu persis berapa kali akan dilakukan.

## while

Syntax `while` memiliki dua bagian:
1. Kondisional
2. Kode program yang dieksekusi

```javascript
// while(kondisional) {
//   kode program yang dieksekusi
// }

let i = 0;
while(i < 10) {
  console.log("Hello");
  i++;
}
```

Apabila diterjemahkan ke Bahasa Indonesia, `while` adalah **SELAMA TRUE LAKUKAN X**. Dengan pengertian tersebut, maka `while` tepat untuk digunakan pada pengulangan di mana kita hanya tahu kondisi berhentinya saja, tanpa mengetahui berapa banyak pengulangan akan dilakukan.

## do...while

Syntax `do...while` memiliki dua bagian:
1. Kondisional
2. Kode program yang dieksekusi

```javascript
// do {
//   kode program yang dieksekusi
// } while (kondisional)

let i = 0;
do {
  console.log("Hello");
  i++;
} while(i < 10);
```

Apabila diterjemahkan ke Bahasa Indonesia, `do...while` adalah **LAKUKAN X SELAMA TRUE**. Dengan pengertian tersebut, maka `do...while` tepat untuk digunakan pada pengulangan di mana kita hanya tahu kondisi berhentinya saja, tanpa mengetahui berapa banyak pengulangan akan dilakukan.

## while vs do...while

Perbedaan antara `while` dengan `do...while` adalah:
- Pada `while` pengecekan kondisi akan dilakukan terlebih dahulu.
- Pada `do...while` pengecekan kondisi akan dilakukan belakangan.

[**Back to Home**](./../README.md)