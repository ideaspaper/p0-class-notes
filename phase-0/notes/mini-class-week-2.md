[**Back to Home**](./../README.md)

# Variables dan primitive data types

Apa yang dilakukan sebuah program komputer? Mereka menerima input user, melakukan proses, kemudian menghasilkan output. Input user adalah data, sehingga pemrosesan yang dilakukan program komputer adalah terhadap data. Output yang dihasilkan juga merupakan data. Dapat disimpulkan, apabila kita membuat program komputer, maka kita akan selalu berhubungan dengan data.

Bagaimana sebuah program dapat menyimpan data dalam sebuah komputer? Jawabannya adalah dengan menggunakan memori.

Variable, secara sederhana, dapat diartikan sebagai memori. Kita bisa memasukkan data-data yang perlu untuk disimpan ke dalam variable. Variable pada bahasa pemrograman JavaScript dapat dibuat menggunakan keyword `var`, `let`, `const`.

```javascript
// Contoh deklarasi variable
var variable1 = 10; // kita memesan memori, kita beri nama sebagai variable1, kemudian kita isi dengan data angka 10
var variable2 = 'Sepuluh'; // kita memesan memori, kita beri nama sebagai variable2, kemudian kita isi dengan data string 'Sepuluh'
let variable3 = true; // kita memesan memori, kita beri nama sebagai variable3, kemudian kita isi dengan data boolean true
let variable4 = false; // kita memesan memori, kita beri nama sebagai variable4, kemudian kita isi dengan data boolean false
const pi = 3.1415926535; // kita memesan memori, kita beri nama sebagai pi, kemudian kita isi dengan data konstan angka 3.1415926535
```

Data memiliki banyak tipe. Pada contoh kode program di atas, terdapat 3 tipe data, yaitu: number, string dan boolean. Kita dapat memeriksa tipe suatu data dengan menggunakan `typeof`.

```javascript
console.log(typeof variable1); // kita ambil nilai dari memori, yaitu variable1 (10), kemudian memeriksa tipe datanya dan menampilkannya ke terminal
console.log(typeof variable2); // kita ambil nilai dari memori, yaitu variable2 ('Sepuluh'), kemudian memeriksa tipe datanya dan menampilkannya ke terminal
console.log(typeof variable3); // kita ambil nilai dari memori, yaitu variable3 (true), kemudian memeriksa tipe datanya dan menampilkannya ke terminal
console.log(typeof variable4); // kita ambil nilai dari memori, yaitu variable4 (false), kemudian memeriksa tipe datanya dan menampilkannya ke terminal
console.log(typeof pi); // kita ambil nilai dari memori, yaitu pi (3.1415926535), kemudian memeriksa tipe datanya dan menampilkannya ke terminal
```

Penamaan variable pada bahasa pemrograman JavaScript memiliki aturan sebagai berikut:
- Hanya dapat menggunakan huruf, angka, `_` dan `$`.
- Menggunakan `camelCase` seperti: `tokoBuku`, `angkaTerbesar`, `adaAngkaGanjil`, dst. (best practice)
- Tidak dapat menggunakan reserved keywords, yaitu kata yang sudah digunakan oleh JavaScript seperti: `let`, `var`, `const`, `class`, dll.
- Tidak dapat diawali dengan angka.
- Tidak dapat menggunakan space.

# Scope

Pada ES6, kita dikenalkan dengan variable scoping (ruang lingkup variable). Variable scoping berlaku jika kita menggunakan `let` dan `const`. Apabila sebuah variable dideklarasikan di dalam sebuah scope, maka scope lain tidak dapat mengakses variable tersebut. Sebuah scope diawali dengan `{` dan diakhiri dengan `}`.

```javascript
// Scope 1
{
  const a = 10;
}
// Scope 2
{
  const b = 5;
}
// Scope 3
{
  let c = a + b;
}
```

Apabila kode program di atas dieksekusi maka akan menghasilkan error `ReferenceError: a is not defined`. Hal tersebut karena `a` hanya dikenali pada `Scope 1`.

```javascript
{
  const a = 10;
  const b = 5;
  let c = a + b;
}
```

Apabila kode program di atas dieksekusi maka hasilnya akan benar. Hal tersebut karena `a`, `b` dan `c` terletak pada scope yang sama.

Jika tidak terdapat `{` dan `}`, seperti pada kode program di bawah, itu artinya hanya terdapat satu scope saja, yaitu scope global.

```javascript
const a = 10;
const b = 5;
let c = a + b;
```

# Hoisting

Apabila kita menggunakan `var` untuk proses deklarasi variable, maka JavaScript akan melakukan hoisting. Apa itu hoisting?

> Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution.

```javascript
// Scope 1
{
  var a = 10;
}
// Scope 2
{
  var b = 5;
}
// Scope 3
{
  var c = a + b;
}
```

Kode program di atas akan berjalan dengan benar. Hal tersebut dikarenakan karena proses hoisting dari JavaScript. Perhatikan contoh program di bawah ini.

```javascript
console.log(hoist); // Output: undefined
var hoist = 'The variable has been hoisted.';
```

Program di atas berhasil dieksekusi, namun hasilnya adalah `undefined`. Hal tersebut dikarenakan kode program tersebut akan "diubah" menjadi seperti di bawah oleh JavaScript.

```javascript
var hoist;
console.log(hoist); // Output: undefined
hoist = 'The variable has been hoisted.';
```

> Sering kali, variable hoisting merupakan perilaku dari JavaScript yang tidak dikehendaki. Hal tersebut dikarenakan hoisting akan membuat alur eksekusi program menjadi tidak jelas. Maka dari itu sangat dianjurkan untuk menggunakan `let` atau `const` pada saat melakukan deklarasi variable.

# Conditionals

Conditional, sesuai namanya, program akan melakukan A apabila suatu kondisi terpenuhi (`true`), dan melakukan B apabila kondisi tersebut tidak terpenuhi (`false`). Pada JavaScript kita dapat membuat statement conditional menggunakan syntax `if...else` atau `switch...case`.

```javascript
if (kondisi1) {
  // Kode yang akan dieksekusi jika kondisi1 true
} else if (kondisi2) {
  // Kode yang akan dieksekusi jika kondisi1 false dan kondisi2 true
} else {
  // Kode yang akan dieksekusi jika kondisi1 dan kondisi2 false
}
```

> Bentuk `if...else` yang valid adalah sebagai berikut:
> ```javascript
> if (kondisi) {
> // Kode yang akan dieksekusi jika kondisi true
> }
> ```
>
> ```javascript
> if (kondisi) {
> // Kode yang akan dieksekusi jika kondisi true
> } else {
> // Kode yang akan dieksekusi jika kondisi false
> }
> ```
>
> ```javascript
> if (kondisi1) {
> // Kode yang akan dieksekusi jika kondisi1 true
> } else if (kondisi2) {
> // Kode yang akan dieksekusi jika kondisi1 false dan kondisi2 true
> }
> ```
>
> ```javascript
> if (kondisi1) {
> // Kode yang akan dieksekusi jika kondisi1 true
> } else if (kondisi2) {
> // Kode yang akan dieksekusi jika kondisi1 false dan kondisi2 true
> } else {
> // Kode yang akan dieksekusi jika kondisi 1 dan kondisi2 false
> }
> ```

```javascript
switch(variable) {
  case nilai1:
    // Kode yang akan dieksekusi jika variable sama dengan nilai1
    break;
  case nilai2:
    // Kode yang akan dieksekusi jika variable sama dengan nilai2
    break;
  case nilai3:
    // Kode yang akan dieksekusi jika variable sama dengan nilai3
    break;
  default:
    // Kode yang akan dieksekusi jika variable tidak sama dengan nilai1, nilai2, ataupun nilai3
    break;
}
```

Kita dapat membuat kondisi menggunakan operator pembanding `>`, `<`, `>=`, `<=`, `==`, `!=`, `===`, `!==`.

# Functions

Function merupakan kode program yang dikelompokkan menjadi satu bagian. Alasan dari pengelompokan ini adalah kode program tersebut sering digunakan berkali-kali. Pembuatan function dapat dilakukan menggunakan syntax seperti di bawah ini.

```javascript
function penambahan() {
  // Kode program
  let hasil = 10 + 5;
}
```

## Parameter

Parameter digunakan untuk membuat function yang kita buat menjadi dinamis. Cara penggunaan parameter pada saat pembuatan function adalah seperti di bawah.

```javascript
function penambahan(a, b) {
  // Kode program
  let hasil = a + b;
}
```

## Return

Sebuah function dapat memberikan nilai kembalian (`return`). `return` dapat digunakan jika kita **hendak melakukan proses lebih lanjut terhadap data yang telah diolah oleh function**.

```javascript
function penambahan(a, b) {
  // Kode program
  let hasil = a + b;
  return hasil;
}

function perkalian(a, b) {
  // Kode program
  let hasil = a * b;
  return hasil;
}

console.log(perkalian(penambahan(2, 3), penambahan(1, 2)));
```

Pada contoh kode program di atas, `return` dari function `penambahan` digunakan sebagai argumen pemanggilan function `perkalian`. Kita tidak dapat menggunakan hasil dari function `penambahan` sebagai argumen function perkalian jika kita **mengganti `return hasil` dengan `console.log(hasil)`**.

# Strings

String merupakan salah satu tipe data primitive pada JavaScript. Sebuah string akan berisi kumpulan karakter seperti di bawah.

```javascript
let str1 = "Ini adalah sebuah string";
let str2 = "0123456789";
let str3 = "Variable str2 merupakan string";
let str4 = "Meskipun isi str2 adalah angka, angka-angka tersebut adalah karakter, bukan number";
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

**Tips**: Jika tidak yakin dengan hasil penambahan string, cobalah terlebih dahulu dengan `console.log()`.

Bagaimana dengan operasi yang lainnya, seperti pengurangan, perkalian, pembagian, dll.?

> Silahkan melakukan eksperimen mandiri dengan `console.log()`.

## String literals

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

## Length dan indexing

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

# Arrays

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

## Mengapa kita membutuhkan array?

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

## Length dan indexing

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

## Menambahkan elemen ke array

Kita **TIDAK DAPAT menambahkan elemen ke array dengan operator `+`** seperti pada string. Penambahan elemen ke array dapat dilakukan menggunakan dua buah built-in function berikut.

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

## Menghapus elemen array

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

## Memeriksa apakah array kosong

Sebuah array dimungkinkan untuk kosong (tidak memiliki elemen sama sekali). Kita **TIDAK DAPAT** melakukan pengecekan sebuah array kosong seperti di bawah ini.

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

# Pseudocode and Loopings

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

> **DRY (Don't Repeat Yourself)**. Pekerjaan manual yang sama dan dilakukan berkali-kali akan memperbesar kemungkinan terjadinya human error.

## for

Syntax `for` memiliki empat bagian:
1. Inisialisasi
2. Kondisional
3. Increment/decrement
4. Kode program yang dieksekusi

> **Syntax**
> 
> ```
> for (1. Inisialisasi; 2. Kondisional; 3. Increment/decrement) {
>   4. Kode program yang dieksekusi
> }
> ```
> 
> **Pseudocode**
> 
> ```
> FOR i FROM 0 TO 9 INCREMENT BY 1
>   DISPLAY 'Hello'
> END FOR
> ```
> 
> **Example**
> 
> ```javascript
> for (var i = 0; i < 10; i++) {
>   console.log("Hello");
> }
> ```

Apabila diterjemahkan ke Bahasa Indonesia, `for` adalah **LAKUKAN X SEBANYAK Y KALI**. Dengan pengertian tersebut, maka `for` tepat untuk digunakan pada pengulangan yang kita tahu persis berapa kali akan dilakukan.

## while

Syntax `while` memiliki dua bagian:
1. Kondisional
2. Kode program yang dieksekusi

> **Syntax**
> 
> ```
> while(1. Kondisional) {
>   2. Kode program yang dieksekusi
> }
> ```
> 
> **Pseudocode**
> 
> ```
> STORE i as NUMBER WITH VALUE 0
> WHILE i LESS THAN 10
>   DISPLAY 'Hello'
>   SET i TO i + 1
> END WHILE
> ```
> 
> **Example**
> 
> ```javascript
> var i = 0;
> while(i < 10) {
>   console.log("Hello");
>   i++;
> }
> ```

Apabila diterjemahkan ke Bahasa Indonesia, `while` adalah **SELAMA TRUE LAKUKAN X**. Dengan pengertian tersebut, maka `while` tepat untuk digunakan pada pengulangan di mana kita hanya tahu kondisi berhentinya saja, tanpa mengetahui berapa banyak pengulangan akan dilakukan.

## do...while

Syntax `do...while` memiliki dua bagian:
1. Kondisional
2. Kode program yang dieksekusi

> **Syntax**
> 
> ```
> do {
>   1. Kode program yang dieksekusi
> } while (2. Kondisional)
> ```
> 
> **Pseudocode**
> 
> ```
> STORE i AS NUMBER WITH VALUE 0
> DO
>   DISPLAY 'Hello'
>   SET i TO i + 1
> WHILE i LESS THAN 10
> ```
> 
> **Example**
> 
> ```javascript
> var i = 0;
> do {
>   console.log("Hello");
>   i++;
> } while(i < 10);
> ```

Apabila diterjemahkan ke Bahasa Indonesia, `do...while` adalah **LAKUKAN X SELAMA TRUE**. Dengan pengertian tersebut, maka `do...while` tepat untuk digunakan pada pengulangan di mana kita hanya tahu kondisi berhentinya saja, tanpa mengetahui berapa banyak pengulangan akan dilakukan.

## while vs do...while

Perbedaan antara `while` dengan `do...while` adalah:
- Pada `while` pengecekan kondisi akan dilakukan terlebih dahulu.
- Pada `do...while` pengecekan kondisi akan dilakukan belakangan.

## break

`break` merupakan statement yang dapat digunakan untuk mengakhiri looping. Sebagai contoh, perhatikan kode program di bawah:

```javascript
for (var i = 0; i < 10; i++) {
  console.log('Hello');
  break;
}
```

Hasil yang didapatkan dari mengeksekusi kode program tersebut hanyalah sebuah text `'Hello'`. Setelah `'Hello'` ditampilkan, komputer akan mengeksekusi statement `break`, sehingga proses looping terhenti.

# Practices

## Problem 1

```javascript
/**
 * Buatlah sebuah program yang akan menampilkan pada terminal hasil penambahan dari angka 1 hingga input.
 */

let input = 10;
```

## Problem 2

```javascript
/**
 * Buatlah sebuah program yang akan menampilkan input (per-dua-huruf) pada terminal ke bawah.
 */

let input = 'Aku suka makan es krim';
```

## Problem 3

```javascript
/**
 * Buatlah program yang akan membalik input, kemudian menampilkannya pada terminal.
 */

let input = 'Aku suka makan es krim';
```

## Problem 4

```javascript
/**
 * Buatlah program yang akan membalik input yang bertipe array, kemudian menampilkannya pada terminal.
 */

let input = ['A', 'B', 'C', 'D', 'E'];
```

## Problem 5

```javascript
/**
 * Buatlah sebuah program yang akan menampilkan elemen kelipatan 3 pada sebuah input bertipe array.
 */

let input = ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J'];
```

## Problem 6

```javascript
/**
 * Buatlah sebuah program yang akan menghitung total dari penjumlahan karakter angka pada sebuah string.
 * Total penjumlahan tersebut kemudian ditampilkan pada terminal.
 */

let input = '17 Agustus 2020';
```

## Problem 7

```javascript
/**
 * Buat sebuah program yang akan menghitung banyaknya huruf vokal pada input bertipe string.
 * Tampilkan banyak huruf vokal tersebut pada terminal.
 */

let input = '17 Agustus 2020';
```

## Problem 8

```javascript
/**
 * Buat sebuah program yang akan mencari nilai maksimum pada sebuah input array.
 * Tampilkan nilai maksimum tersebut pada terminal.
 */

let input = [5, 16, 4, 2, 7, 88, 41, 53, 89, 33, 62];
```

## Problem 9

```javascript
/**
 * Buat sebuah program yang akan mencari nilai minimum pada sebuah input array.
 * Tampilkan nilai minimum tersebut pada terminal.
 */

let input = [5, 16, 4, 2, 7, 88, 41, 53, 89, 33, 62];
```

## Problem 10

```javascript
/**
 * Buatlah sebuah program yang akan mengganti semua huruf vokal dan angka pada sebuah input string dengan simbol ★.
 * Tampilkan string yang telah diubah tersebut ke terminal.
 */

let input = '17 Agustus 2020';
```

## Problem 11

```javascript
/**
 * Buat sebuah program yang akan mengurangi masing-masing elemen pada sebuah input array
 * dengan nilai elemen maksimum input array tersebut. Tampilkan hasilnya pada terminal.
 */

let input = [5, 16, 4, 2, 7, 88, 41, 53, 89, 33, 62]; // Nilai maksimum adalah 89. Maka semua elemen akan dikurangi dengan 89.
```

[**Back to Home**](./../README.md)