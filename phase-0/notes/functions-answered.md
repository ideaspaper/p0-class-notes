[**Back to Home**](./../README.md)

# Functions

Apabila kita memiliki beberapa baris kode program yang sering kita gunakan, maka terdapat dua cara untuk menggunakannya:

1. Melakukan copy-paste baris kode program tersebut setiap kali kita memerlukannya.
2. Membuat sebuah function untuk "membungkus" kode program tersebut. Setiap saat kita memerlukan kode program tersebut, kita hanya perlu memanggil function yang telah kita buat sebelumnya.

Function merupakan kode program yang dikelompokkan menjadi satu bagian. Beberapa keuntungan dari penggunaan function adalah sebagai berikut:

- Kita tetap menganut prinsip DRY (Don't Repeat Yourself), sehingga human error akan diminimalisir.
- Ukuran kode program akan lebih kecil.
- Lebih mudah untuk melakukan debug.

> **Syntax**
>
> ```
> function namaFunction(parameter) {
>   // Kode program
> }
> ```
>
> `parameter` bersifat opsional.
>
> **Pseudocode**
> ```
> BEGIN penambahan
>   DISPLAY 10 + 5
> END penambahan
>
> INVOKE(penambahan)
> ```
>
> **Example**
>
> ```javascript
> function penambahan() {
>   console.log(10 + 5);
> }
>
> penambahan();
> ```

## Nama Function

Penamaan function pada JavaScript memiliki convention yang sama dengan penamaan variable:

- Hanya dapat menggunakan huruf, angka, `_` dan `$`.
- Menggunakan `camelCase` seperti: `reverseString`, `getMedian`, `getAverage`, dst. (best practice)
- Tidak dapat menggunakan reserved keywords, yaitu kata yang sudah digunakan oleh JavaScript seperti: `let`, `var`, `const`, `class`, dll.
- Tidak dapat diawali dengan angka.
- Tidak dapat menggunakan space.

## Parameters dan Argument

Apabila sebuah function kita deklarasikan dengan sebuah parameter, kita dapat memanggil function tersebut dengan argument.

```javascript
// Membuat sebuah function penambahan dengan a dan b sebagai parameter.
function penambahan(a, b) {
  console.log(a + b);
}

// Memanggil function penambahan dengan argument 10 dan 5.
// 10 akan dikenali oleh function penambahan sebagai a.
// 5 akan dikenali oleh function penambahan sebagai b.
penambahan(10, 5);
```

Salah satu tujuan dari parameter adalah agar kode program dalam function menjadi dinamis. Kita dapat membuat kode program dalam function bekerja sesuai dengan argument saat kita memanggil function tersebut.

Parameter pada pseudocode dapat dituliskan dengan `PASS IN: parameter1, parameter2`.

## Default Parameters

Parameter function dapat diberi nilai default. Nilai tersebut akan digunakan apabila pada pemanggilan function kita tidak menyertakan nilai sebagai argument. 

```javascript
function penambahan(a = 10, b = 5) {
  console.log(a + b);
}

penambahan(); // 15
penambahan(1, 2); // 3
```

Karena nilai argument selalu dibaca dari kiri ke kanan sesuai dengan urutan parameter, maka parameter dengan nilai default selalu dituliskan di akhir. Contoh kasus apabila default parameter tidak diletakkan di akhir adalah seperti kode program di bawah.

```javascript
function tampilkan(x = 1, y) {
  console.log(x, y);
}

tampilkan();   // 1 undefined
tampilkan(2);  // 2 undefined
```

## Return

Sebuah function dapat memberikan nilai kembalian (`return`). `return` dapat digunakan jika kita **hendak melakukan proses lebih lanjut terhadap data yang telah diolah oleh function**.

```javascript
function penambahan(a, b) {
  let hasil = a + b;
  return hasil;
}

function perkalian(a, b) {
  let hasil = a * b;
  return hasil;
}

console.log(perkalian(penambahan(2, 3), penambahan(1, 2)));
```

Pada contoh kode program di atas, `return` dari function `penambahan` digunakan sebagai argument pemanggilan function `perkalian`. Kita tidak dapat menggunakan hasil dari function `penambahan` sebagai argument pemanggilan function `perkalian` jika kita **mengganti `return hasil` dengan `console.log(hasil)`**.

> - Apabila eksekusi kode program pada function menemukan statement `return`, maka proses eksekusi function akan berhenti.
> - Sebuah function hanya dapat me-`return` sebuah value saja.

Return pada pseudocode dapat dituliskan dengan `PASS OUT: returnValue`.

## Scope Function

- Parameter yang disertakan saat proses deklarasi function **hanya akan dikenali di dalam scope function itu saja**.
  ```javascript
  function penambahan(a, b) {
    return a + b;
  }
  penambahan(10, 5);
  console.log(a); // ReferenceError: a is not defined
  ```
- Variable yang dideklarasikan di dalam function **hanya akan dikenali di dalam scope function itu saja**.
  ```javascript
  function penambahan() {
    let a = 10;
    var b = 5;
    return a + b;
  }
  console.log(a); // ReferenceError: a is not defined
  console.log(b); // ReferenceError: b is not defined
  ```

## Practices

```javascript
/**
 * Buatlah sebuah function untuk membalik sebuah input string.
 */

/**
 * PSEUDOCODE
 * 
 * BEGIN reverseString
 *   PASS IN:  strIn
 *   STORE ret AS STRING WITH VALUE ''
 *   FOR i FROM (LENGTH OF strIn - 1) TO 0 DECREMENT BY 1
 *     SET ret TO ret + strIn INDEX i
 *   END FOR
 *   PASS OUT: ret
 * END reverseString
 * 
 * DISPLAY INVOKE(reverseString('Hello world!'))
 */

function reverseString(strIn) {
  let ret = '';
  for (let i = strIn.length - 1; i >= 0; i--) {
    ret += strIn[i];
  }
  return ret;
}

console.log(reverseString('Hello world!'));
```

```javascript
/**
 * Buatlah sebuah function untuk menjumlahkan angka genap dari 1 hingga input number.
 */

/**
 * PSEUDOCODE
 * 
 * BEGIN sumEven
 *   PASS IN:  numIn
 *   STORE ret AS NUMBER WITH VALUE 0
 *   FOR i FROM 1 TO numIn INCREMENT BY 1
 *     IF (i MODULUS 2) EQUAL 0
 *       SET ret TO ret + i
 *     END IF
 *   END FOR
 *   PASS OUT: ret
 * END sumEven
 * 
 * DISPLAY INVOKE(sumEven(10))
 */

function sumEven(numIn) {
  let ret = 0;
  for (let i = 1; i <= numIn; i++) {
    if (i % 2 === 0) {
      ret += i;
    }
  }
  return ret;
}

console.log(sumEven(10)); // 30
```

[**Back to Home**](./../README.md)