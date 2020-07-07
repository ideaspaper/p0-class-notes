# Advanced Conditional

## `switch-case`

### Bentuk Dasar

```javascript
switch (expression) {
  case nilai1:
    // Statement yang akan dieksekusi
    break;
  case nilai2:
    // Statement yang akan dieksekusi
    break;
}
```

### Latihan 1

```javascript
/**
 * Berdasarkan suatu angka 1 hingga 5, tampilkan output sebagai berikut:
 *   1: ★☆☆☆☆
 *   2: ★★☆☆☆
 *   3: ★★★☆☆
 *   4: ★★★★☆
 *   5: ★★★★★
 *
 * Kerjakan dengan statement switch-case.
 */

var input1 = 3;

switch (input1) {
  case 1:
    console.log("★☆☆☆☆");
    break;
  case 2:
    console.log("★★☆☆☆");
    break;
  case 3:
    console.log("★★★☆☆");
    break;
  case 4:
    console.log("★★★★☆");
    break;
  case 5:
    console.log("★★★★★");
    break;
}
```

### `default` pada `switch-case`

Apabila tidak ada case yang cocok dengan hasil dari expression, maka statement yang akan dieksekusi adalah statement yang ada pada default.

```javascript
switch (expression) {
  case nilai1:
    // Statement yang akan dieksekusi
    break;
  case nilai2:
    // Statement yang akan dieksekusi
    break;
  default:
  // Statement yang akan dieksekusi
}
```

### Latihan 2

```javascript
/**
 * Berdasarkan suatu angka 1 hingga 5, tampilkan output sebagai berikut:
 *   1: ★☆☆☆☆
 *   2: ★★☆☆☆
 *   3: ★★★☆☆
 *   4: ★★★★☆
 *   5: ★★★★★
 *
 * Apabila angka tersebut di luar range 1 hingga 5, tampilkan 'Invalid'.
 * Kerjakan dengan statement switch-case.
 */

var input2 = 10;

switch (input2) {
  case 1:
    console.log("★☆☆☆☆");
    break;
  case 2:
    console.log("★★☆☆☆");
    break;
  case 3:
    console.log("★★★☆☆");
    break;
  case 4:
    console.log("★★★★☆");
    break;
  case 5:
    console.log("★★★★★");
    break;
  default:
    console.log("Invalid");
}
```

### Statement `break` pada `switch-case`

The switch statement evaluates an expression, matching the expression's value to a case clause, and executes statements associated with that case, as well as statements in cases that follow the matching case. [MDN - Switch](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch).

```javascript
switch (expression) {
  case nilai1:
  // Statement yang akan dieksekusi
  case nilai2:
  // Statement yang akan dieksekusi
}
```

### Latihan 3

```javascript
/**
 * Berdasarkan suatu angka 1 hingga 5, tampilkan output sebagai berikut:
 *   1: ★
 *   2: ★★
 *   3: ★★★
 *   4: ★★★★
 *   5: ★★★★★
 *
 * Apabila angka tersebut di luar range 1 hingga 5, tampilkan 'Invalid'.
 * Kerjakan dengan statement switch-case tanpa menggunakan statement break.
 */

var input3 = 3;
var output = "";

switch (input2) {
  case 5:
    output = output + "★";
  case 4:
    output = output + "★";
  case 3:
    output = output + "★";
  case 2:
    output = output + "★";
  case 1:
    output = output + "★";
  default:
    output = "Invalid";
}

console.log(output);
```

## `if-if` dan `if-else`

### `if-if`

Pengecekan akan dilakukan pada semua if.

```javascript
var a = 7;
if (a < 10) {
  a = a + 2;
}
if (a < 10) {
  a = a + 2;
}
console.log(a);
```

### `if-else`

Pengecekan akan dilakukan selama belum ditemukan ekspresi yang bernilai true. Apabila sudah ditemukan ekspresi yang bernilai true, pengecekan akan dihentikan.

```javascript
var b = 7;
if (b < 10) {
  b = b + 2;
} else if (b < 10) {
  b = b + 2;
}
console.log(b);
```

### Latihan 4

```javascript
/**
 * Sebuah bengkel membutuhkan program untuk menghitung tarif berdasarkan service
 * yang diberikan kepada konsumen.
 * Tarif dari service yang diberikan adalah sebagai berikut:
 *   - Ganti oli: 10000
 *   - Ganti ban: 7500
 *   - Pompa ban: 2500
 *   - Tambal ban: 25000
 *
 * Konsumen dapat meminta lebih dari satu jenis service kepada bengkel tersebut.
 */

var gantiOli = true;
var gantiBan = true;
var pompaBan = true;
var tambalBan = true;

var total = 0;

if (gantiOli) {
  total += 10000;
}
if (gantiBan) {
  total += 7500;
}
if (pompaBan) {
  total += 2500;
}
if (tambalBan) {
  total += 25000;
}

console.log(total);
```

## Nested Conditionals

Statement conditional bisa terdapat di dalam statement conditional lainnya.

```javascript
if (expression1) {
  if (expression2) {
    // Statements to execute
  } else {
    // Statements to execute
  }
} else {
  if (expression3) {
    // Statements to execute
  } else {
    // Statements to execute
  }
}
```

```javascript
switch (expression1) {
  case a:
    switch (expression2) {
      case c:
        // Statements to execute
        break;
      case d:
        // Statements to execute
        break;
    }
    break;
  case b:
    switch (expression3) {
      case e:
        // Statements to execute
        break;
      case f:
        // Statements to execute
        break;
    }
    break;
}
```

### Latihan 5

```javascript
/**
 * Kegiatan seorang pengembara dapat ditentukan berdasarkan relasi
 * antara rasa lapar dan uang yang dimilikinya saat itu.
 * Relasi tersebut adalah sebagai berikut:
 *   - Jika lapar, maka pengembara akan:
 *       - Makan: jika memiliki uang
 *       - Tidur :jika tidak memiliki uang
 *   - Jika tidak lapar, maka pengembara akan:
 *       - Nyemil: jika memiliki uang
 *       - Minum air: jika tidak memiliki uang
 *
 * Buatlah program untuk mensimulasikan kegiatan pengembara tersebut.
 */

var lapar = false;
var uang = false;

if (lapar) {
  if (uang) {
    console.log("Makan");
  } else {
    console.log("Tidur");
  }
} else {
  if (uang) {
    console.log("Nyemil");
  } else {
    console.log("Minum air");
  }
}
```

## Additional Topics

### `Math`

Built-in functions yang umum digunakan dari `Math` adalah:

- `floor`: Pembulatan ke bawah
- `ceil`: Pembulatan ke atas
- `round`:
  - Apabila bagian desimal dari sebuah angka >= 0.5, maka dilakukan pembulatan ke atas.
  - Apabila bagian desimal dari sebuah angka < 0.5, maka dilakukan pembulatan ke bawah.

```javascript
var number = 3.5;
console.log(Math.floor(number));
console.log(Math.ceil(number));
console.log(Math.round(number));
console.log(Math.random()); // Output: 0 (inclusive) hingga 1 (exclusive)
```

### Latihan 6

```javascript
/**
 * Buat kode program untuk memberikan angka random dari 0 - 9.
 */

var hasilRandom1 = Math.random() * 10;
hasilRandom1 = Math.floor(hasilRandom1);
console.log(hasilRandom1);
```

### Latihan 7

```javascript
/**
 * Buat kode program untuk memberikan angka random dari 1 - 10.
 */

var hasilRandom2 = Math.random() * 10;
hasilRandom2 = Math.floor(hasilRandom2) + 1;
console.log(hasilRandom2);
```

### `substring`

`str.substring(indexStart[, indexEnd])`

- `indexStart`: The index of the first character to include in the returned substring.
- `indexEnd`: The index of the first character to exclude from the returned substring. (Optional).

```javascript
var string = "0123456789";
// Tampilkan 456
console.log(string.substring(4, 7));
// Tampilkan 789
console.log(string.substring(7));
console.log(string.substring(7, string.length));
```

[Back to Home](./../README.md)
