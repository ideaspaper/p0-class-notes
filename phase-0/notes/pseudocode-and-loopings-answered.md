[**Back to Home**](./../README.md)

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
> STORE i WITH 0
> WHILE i LESS THAN 10
>   DISPLAY 'Hello'
>   SET i WITH i PLUS 1
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
> STORE i WITH 0
> DO
>   DISPLAY 'Hello'
>   SET i WITH i PLUS 1
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

## Infinite Loop

```javascript
// Salah kondisi atau variable yang di-increment
var j = 0;
for (var i = 0; i < 10; j++) {
  console.log(j);
}

// Salah menentukan decrement/increment
for (var i = 10; i > 0; i++) {
  console.log(i);
}
```

## Practices

```javascript
/**
 * Diberikan sebuah string input. Tampilkan semua karakter pada string tersebut ke bawah pada terminal.
 * Buatlah pseudocode beserta kode programnya.
 */

/**
 * PSEUDOCODE
 * 
 * STORE input WITH ANY STRING
 * 
 * FOR i FROM 0 TO (LENGTH OF input - 1) INCREMENT BY 1
 *   DISPLAY input INDEX i
 * END FOR
 */

var input = 'Hello World';

// Your code here
for (var i = 0; i < input.length; i++) {
  console.log(input[i])
}
```

```javascript
/**
 * Diberikan sebuah string input. Tampilkan per-dua karakter dari string tersebut ke bawah pada terminal.
 * Buatlah pseudocode beserta kode programnya.
 * 
 * Contoh:
 *   Input  : 'Hello World'
 *   Output : 'He'
 *            'll'
 *            'o '
 *            'Wo'
 *            'rl'
 *            'd'
 */

/**
 * PSEUDOCODE
 * 
 * STORE input WITH ANY STRING
 * 
 * FOR i FROM 0 TO (LENGTH OF input - 1) INCREMENT BY 2
 *   STORE output WITH (input INDEX i)
 *   IF i + 1 LESS THAN LENGTH OF input
 *     SET output WITH output CONCAT WITH input INDEX (i + 1)
 *   END IF
 *   DISPLAY output
 * END FOR
 */

var input = 'Hello World';

// Your code here
for (var i = 0; i < input.length; i += 2) {
  var output = input[i];
  if (i + 1 < input.length) {
    output += input[i + 1]
  }
  console.log(output);
}
```

```javascript
/**
 * Buatlah sebuah pseudocode dan kode program yang akan menjumlahkan semua angka genap dari 1 hingga input.
 */

/**
 * PSEUDOCODE
 * 
 * STORE input WITH 10
 * STORE hasil WITH 0
 * 
 * FOR i FROM 1 TO input INCREMENT BY 1
 *   IF i MODULUS 2 EQUAL 0
 *     SET hasil WITH hasil PLUS i
 *   END IF
 * END FOR
 * 
 * DISPLAY hasil
 */

var input = 10;

// Your code here
var store = 0;

for (var i = 1; i <= input; i++) {
  if (i % 2 === 0) {
    store += i;
  }
}

console.log(store);
```

```javascript
/**
 * Buatlah sebuah program yang akan menghitung berapa kali seseorang harus melempar dadu sehingga mendapatkan angka 6.
 * Tampilkan hasil perhitungan tersebut pada terminal.
 */

/**
 * PSEUDOCODE
 * 
 * STORE hasilLempar WITH 0
 * STORE totalLempar WITH 0
 * 
 * DO
 *   SET hasilLempar WITH RANDOM NUMBER BETWEEN 1 AND 6
 * WHILE hasilLempar NOT EQUAL 6
 * 
 * DISPLAY totalLempar
 */

var hasilLempar = 0;
var totalLempar = 0;

// Your code here
do {
  hasilLempar = Math.floor(Math.random() * 6) + 1;
  totalLempar++;
} while (hasilLempar !== 6)

console.log(totalLempar);
```

[**Back to Home**](./../README.md)
