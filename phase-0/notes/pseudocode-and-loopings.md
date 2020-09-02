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
 */

var input = 'Hello World';

// Your code here
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
 */

var input = 'Hello World';

// Your code here
```

```javascript
/**
 * Buatlah sebuah pseudocode dan kode program yang akan menjumlahkan semua angka genap dari 1 hingga input.
 */

/**
 * PSEUDOCODE
 */

var input = 10;

// Your code here
```

```javascript
/**
 * Buatlah sebuah program yang akan menghitung berapa kali seseorang harus melempar dadu sehingga mendapatkan angka 6.
 * Tampilkan hasil perhitungan tersebut pada terminal.
 */

/**
 * PSEUDOCODE
 */

var hasilLempar = 0;
var totalLempar = 0;

// Your code here
```

[Answers](./pseudocode-and-loopings-answered.md)

[**Back to Home**](./../README.md)
