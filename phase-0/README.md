# Table of Contents
- [HTML](#html)
- [CSS](#css)
- [Terminal](#terminal)
- [Review: HTML and CSS](#review-html-and-css)
- [Algorithm and Pseudocode](#algorithm-and-pseudocode)
- [Conditional and Primitive Data Types](#conditional-and-primitive-data-types)
- [Nested Conditional](#nested-conditional)
- [Iteration in Pseudocode and JavaScript](#iteration-in-pseudocode-and-javascript)
- [Nested Iteration](#nested-iteration)
- [Review: Conditional and Iteration](#review-conditional-and-iteration)
- [Function](#function)
- [Array](#array)
- [Review: Array](#review-array)
- [Multidimensional Array](#multidimensional-array)
- [Review: Function, Array and Multidimensional Array](#review-function-array-and-multidimensional-array)
- [Modular Functions](#modular-functions)
- [Review: Up to Modular Functions](#review-up-to-modular-functions)
- [Object Literal](#object-literal)
- [Array of Object](#array-of-object)
- [Tracing and Debugging](#tracing-and-debugging)
- [Review: All](#review-all)
- [Local Git](#local-git)
- [Git Branch, Git Merge, GitHub Pull Request and GitHub.io](#git-branch-git-merge-github-pull-request-and-github.io)


# HTML
```html
```

# CSS
```css
```

# Terminal
[Terminal](./assets/terminal-git-and-github.pdf)

# Review: HTML and CSS
```html
```

# Algorithm and Pseudocode

## Algoritma
1. Algoritma tidak sama dengan logaritma.
2. Algoritma merupakan langkah-langkah yang harus diikuti dalam menyelesaikan suatu permasalahan.
3. Algoritma dapat berupa rangkaian kalimat dalam bahasa sehari-hari, ataupun berupa visual dalam bentuk flowchart.
4. Algoritma digunakan agar penyelesaian suatu masalah dapat dilakukan secara sistematis.

```bash
Case: Membuat soda gembira (pada umumnya).

Algoritma:
  1. Siapkan gelas kosong.
  2. Tuang air soda secukupnya ke dalam gelas.
  3. Tuang susu kental manis secukupnya ke dalam gelas.
  4. Tuang sirup secukupnya ke dalam gelas.
  5. Aduk hingga merata.
  6. Masukkan es batu.
```

```bash
Case: Menyiapkan komputer untuk mulai belajar JavaScript (pada umumnya).

Algoritma:
  1. Siapkan komputer dengan OS Ubuntu atau macOS. (opsional)
  2. Download dan install Node.js.
  3. Download dan install Visual Studio Code.
  4. Buat program 'Hello World' sederhana.
  5. Jalankan program 'Hello World' tersebut.
```

Contoh algoritma: [How to Walk Gracefully](https://www.wikihow.com/Walk-Gracefully)

## Pseudocode
1. Dibuat menggunakan bahasa Inggris.
2. Bahasa terstruktur yang digunakan untuk mendeskripsikan algoritma secara detil.
3. Pseudocode digunakan agar kita lebih fokus kepada perancangan logic suatu program tanpa dipusingkan dengan syntax bahasa pemrograman yang akan digunakan nantinya.
4. Pseudocode yang baik adalah pseudocode yang dapat dipahami dengan mudah.

```bash
Case: Menghitung luas segitiga.

Pseudocode:
  INIT alas AS NUMBER WITH ANY VALUE
  INIT tinggi AS NUMBER WITH ANY VALUE
  INIT luas AS NUMBER WITH 0
  COMPUTE luas AS 0.5 * alas * tinggi
  DISPLAY luas
```

```bash
Case: Menghitung kecepatan

Pseudocode:
  INIT jarak AS NUMBER WITH ANY VALUE
  INIT waktu AS NUMBER WITH ANY VALUE
  INIT kecepatan AS NUMBER WITH 0
  COMPUTE kecepatan AS jarak / waktu
  DISPLAY kecepatan
```

[Pseudocode Standard - Dr. John Dalbey](./assets/john-dalbey-pseudocode.pdf)

# Conditional and Primitive Data Types
```javascript
```

# Nested Conditional
Selain `if-else` kita dapat menggunakan `switch-case` untuk keperluan conditional. Penggunaan `switch-case` membuat kode program relatif lebih mudah untuk dibaca, sedangkan penggunaan `if-else` memberikan opsi yang lebih fleksibel.

## `switch-case`
```javascript
switch (variable) {
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

Nilai `variable` yang terdapat pada `switch` akan diperiksa. Apabila nilai tersebut `=== nilai1` maka statement di dalam `case nilai1:` akan dieksekusi. Apabila nilai tersebut `=== nilai2` maka statement di dalam `case nilai2:` akan dieksekusi. Apabila nilai tersebut `!== nilai1` dan `!== nilai2` maka statement di dalam `default:` akan dieksekusi.

## Penggunaan `switch-case`
```javascript
/**
 * Ubah angka 0 - 10 ke dalam bahasa Indonesia.
 * Gunakan Switch-Case untuk menyelesaikan permasalahan ini.
 */

/**
 * INIT angka AS NUMBER WITH ANY VALUE
 * 
 * SWITCH angka
 *   CASE 0:
 *     DISPLAY 'Nol'
 *     BREAK
 *   CASE 1:
 *     DISPLAY 'Satu'
 *     BREAK
 *   CASE 2:
 *     DISPLAY 'Dua'
 *     BREAK
 *   CASE 3:
 *     DISPLAY 'Tiga'
 *     BREAK
 *   CASE 4:
 *     DISPLAY 'Empat'
 *     BREAK
 *   CASE 5:
 *     DISPLAY 'Lima'
 *     BREAK
 *   CASE 6:
 *     DISPLAY 'Enam'
 *     BREAK
 *   CASE 7:
 *     DISPLAY 'Tujuh'
 *     BREAK
 *   CASE 8:
 *     DISPLAY 'Delapan'
 *     BREAK
 *   CASE 9:
 *     DISPLAY 'Sembilan'
 *     BREAK
 *   CASE 10:
 *     DISPLAY 'Sepuluh'
 *     BREAK
 *   DEFAULT:
 *     DISPLAY 'Angka belum di-support'
 * END SWITCH
 */

let angka = 9;

switch (angka) {
  case 0:
    console.log('Nol');
    break;
  case 1:
    console.log('Satu');
    break;
  case 2:
    console.log('Dua');
    break;
  case 3:
    console.log('Tiga');
    break;
  case 4:
    console.log('Empat');
    break;
  case 5:
    console.log('Lima');
    break;
  case 6:
    console.log('Enam');
    break;
  case 7:
    console.log('Tujuh');
    break;
  case 8:
    console.log('Delapan');
    break;
  case 9:
    console.log('Sembilan');
    break;
  case 10:
    console.log('Sepuluh');
    break;
  default:
    console.log('Angka belum di-support');
}
```

Untuk memahami penggunaan statement `break`, coba jalankan contoh kode program di bawah.

```javascript
/**
 * Ubah nilai variable angka menjadi 0, 1, 2, kemudian 3.
 * Amati output program.
 */

let angka = 1;

switch (angka) {
  case 0:
    console.log('Nol');
  case 1:
    console.log('Satu');
  case 2:
    console.log('Dua');
  case 3:
    console.log('Tiga');
    break;
  case 4:
    console.log('Empat');
    break;
  case 5:
    console.log('Lima');
    break;
  case 6:
    console.log('Enam');
    break;
  case 7:
    console.log('Tujuh');
    break;
  case 8:
    console.log('Delapan');
    break;
  case 9:
    console.log('Sembilan');
    break;
  case 10:
    console.log('Sepuluh');
    break;
  default:
    console.log('Angka belum di-support');
}
```

## Ternary Operator

Selain `if-else` dan `switch-case`, terdapat pula ternary operator `(?:)`.

```javascript
let a = 10;

a > 5 ? console.log('lebih dari 5') : console.log('kurang dari 5');
```

- `a > 5` merupakan bagian conditional.
- Setelah `?`, yaitu `console.log('lebih dari 5')`, merupakan bagian yang akan dieksekusi apabila hasil evaluasi bagian conditional bernilai `true`.
- Setelah `:`, yaitu `console.log('kurang dari 5')`, merupakan bagian yang akan dieksekusi apabila hasil evaluasi bagian conditional bernilai `false`.

Penggunaan ternary operator dapat membuat kode program lebih mudah untuk di baca. Namun apabila di dalam ternary operator terdapat ternary operator lain (nested), maka pembacaan kode program akan menjadi lebih susah.

## Nested `if-else`
Sebuah conditional dapat memiliki conditional lain di dalamnya. Hal ini disebut juga sebagai nested conditionals. Di bawah merupakan contoh permasalahan yang dapat diselesaikan dengan nested conditionals.

```javascript
/**
 * Sebuah wahana membutuhkan 3 buah kriteria untuk penumpang yaitu
 *   - Umur di dalam range 15 tahun hingga 60 tahun
 *   - Tinggi badan setidaknya 150 cm
 *   - Tidak memiliki penyakit jantung
 * 
 * Buatlah pseudocode dan kode program untuk mensimulasikan kriteria wahana tersebut.
 */

/**
 * INIT umur AS NUMBER WITH ANY VALUE
 * INIT tinggi AS NUMBER WITH ANY VALUE
 * INIT penyakitJantung AS BOOLEAN WITH ANY VALUE
 * 
 * IF umur MORE THAN EQUAL 15 AND umur LESS THAN EQUAL 60
 *   IF tinggi MORE THAN EQUAL 150
 *     IF penyakitJantung EQUAL FALSE
 *       DISPLAY 'Boleh naik wahana'
 *     ELSE
 *       DISPLAY 'Tidak boleh naik wahana karena alasan jantung'
 *     END IF
 *   ELSE
 *     DISPLAY 'Tidak boleh naik wahana karena alasan tinggi badan'
 *   END IF
 * ELSE
 *   DISPLAY 'Tidak boleh naik wahana karena alasan umur'
 * ENDIF
 */

let umur = 13;
let tinggi = 140
let penyakitJantung = true;

if (umur >= 15 && umur <= 60) {
  if (tinggi >= 150) {
    if (penyakitJantung === false) {
      console.log('Boleh naik wahana');
    } else {
      console.log('Tidak boleh naik wahana karena alasan jantung');
    }
  } else {
    console.log('Tidak boleh naik wahana karena alasan tinggi badan');
  }
} else {
  console.log('Tidak boleh naik wahana karena alasan umur');
}
```

## `if-if` vs `if-else`
Hal lain yang perlu diperhatikan adalah penggunaan `if-if` dan `if-else`. Keduanya memiliki alur eksekusi yang berbeda. Pada conditional `if-else`, apabila kondisi pada `if` bernilai `true`, maka kondisi pada `else-if` tidak akan diperiksa, serta statement di dalam `else` tidak akan dieksekusi.

Pada `if-if`, apabila kondisi pada `if` pertama bernilai `true`, kondisi pada `if` kedua tetap akan diperiksa. Lebih jelasnya, jalankan contoh kode program di bawah.

```javascript
let myVar = 7;

if (myVar > 6) {
  console.log('nilai myVar lebih dari 6');
} else if (myVar > 5) {
  console.log('nilai myVar lebih dari 5');
}

if (myVar > 6) {
  console.log('nilai myVar lebih dari 6');
}
if (myVar > 5) {
  console.log('nilai myVar lebih dari 5');
}
```

# Iteration in Pseudocode and JavaScript
[Iteration in Pseudocode and JavaScript](./assets/pseudocode-and-iteration.pdf)


## `for`
```javascript
/**
 * 1. PENGGUNAAN FOR
 * 
 * INIT times AS NUMBER WITH VALUE OF 5
 * FOR loop FROM 0 TO times
 *   DISPLAY 'meow'
 * END FOR
 */

// Code here
let times = 5;
for (let loop = 0; loop <= times; loop++) {
  console.log('meow');
}


/**
 * 2. PENGGUNAAN CONDITIONAL DI DALAM FOR
 * 
 * INIT times AS NUMBER WITH VALUE OF 10
 * FOR loop FROM 1 TO times
 *   IF loop MORE THAN EQUAL 5
 *     DISPLAY loop
 *   END IF
 * END FOR
 */

// Code here
times = 10;
for (let loop = 1; loop <= times; loop++) {
  if (loop >= 5) {
    console.log(loop);
  }
}


/**
 * 3. BENTUK LAIN DARI FOR
 * 
 *   1. for (; [condition];)
 *   2. for ([initial expression 1], [initial expression 2]; [condition 1]; [increment expression 1], [increment expression 2])
 *   3. for (; ;)
 */

// 1. for (; [condition];),
//    sama dengan while (i > 0)
//    Code here
loop = 5;
for (; loop > 0;) {
  console.log(loop);
  loop--;
}

// 2. for ([initial expression 1], [initial expression 2]; [condition]; [increment expression 1], [increment expression 2]),
//    for dapat memiliki lebih dari satu initial expression, lebih dari satu condition, lebih dari satu increment expression
//    Code here
for (let i = 0, j = 9; i < 10; i++, j--) {
  console.log(i, j);
}

// 3. Sama dengan while (true)
//    Code here
for (; ;) {
  console.log('meow');
}
```

## `while`
```javascript
/**
 * 1. PENGGUNAAN WHILE
 * 
 * INIT times AS NUMBER WITH VALUE OF 5
 * WHILE times MORE THAN EQUAL 0
 *   DISPLAY 'meow'
 *   DECREMENT times
 * END WHILE
 */

// Code here
let times = 5;
while (times >= 0) {
  console.log('meow');
  times--;
}

/**
 * 2. PENGGUNAAN CONDITIONAL DI DALAM WHILE
 * 
 * INIT a AS NUMBER WITH ANY VALUE
 * WHILE TRUE
 *   IF a MODULUS 100 EQUAL TO 0
 *     DISPLAY a
 *     BREAK
 *   ELSE
 *     INCREMENT a
 *   END IF
 * END WHILE
 */

// Code here
let a = 75;
while (true) {
  if (a % 100 === 0) {
    console.log(a);
    break;
  } else {
    a++;
  }
}

/**
 * 3. HASIL WHILE BERIKUT SAMA DENGAN IMPLEMENTASI POIN 2
 * 
 * INIT a AS NUMBER WITH ANY VALUE
 * WHILE TRUE
 *   IF a MODULUS 100 EQUAL TO 0
 *     DISPLAY a
 *     BREAK
 *   END IF
 *   INCREMENT a
 * END WHILE
 */

// Code here
a = 75;
while (true) {
  if (a % 100 === 0) {
    console.log(a);
    break;
  }
  a++;
}
```

## `do-while`
```javascript
/**
 * 1. PENGGUNAAN DO-WHILE
 * 
 * INIT times AS NUMBER WITH VALUE OF 5
 * DO
 *   DISPLAY 'meow'
 *   DECREMENT times
 * WHILE times MORE THAN EQUAL 0
 */

// Code here
let times = 5;
do {
  console.log('meow');
  times--;
} while (times >= 0);

/**
 * 2. HASIL WHILE BERIKUT SAMA DENGAN IMPLEMENTASI POIN 1
 * 
 * INIT times AS NUMBER WITH VALUE OF 5
 * WHILE times MORE THAN EQUAL 0
 *   DISPLAY 'meow'
 *   DECREMENT times
 * END WHILE
 */

// Code here
times = 5;
while (times >= 0) {
  console.log('meow');
  times--;
}

/**
 * 3. PENGECEKAN KONDISI DO-WHILE DILAKUKAN DI AKHIR
 * 
 * INIT times AS NUMBER WITH VALUE OF -1
 * DO
 *   DISPLAY 'meow'
 *   DECREMENT times
 * WHILE times MORE THAN EQUAL 0
 */

// Code here
times = -1;
do {
  console.log('meow');
  times--;
} while (times >= 0);

/**
 * 4. PENGECEKAN KONDISI WHILE DILAKUKAN DI AWAL
 * 
 * INIT times AS NUMBER WITH VALUE OF -1
 * WHILE times MORE THAN EQUAL 0
 *   DISPLAY 'meow'
 *   DECREMENT times
 * END WHILE
 */

// Code here
times = -1;
while (times >= 0) {
  console.log('meow');
  times--;
}
```

## Increment and Decrement
```javascript
// ++ merupakan operator increment
// Post increment, ++ akan dieksekusi setelah statement dieksekusi
let temp = 10;
console.log(temp++, temp);
// Pre increment, ++ akan dieksekusi sebelum statement dieksekusi
temp = 10;
console.log(++temp, temp);

// += merupakan compound assignment operator
// temp += 1 memiliki arti temp = a + 1, sama dengan ++temp
temp = 10;
console.log(temp += 1, temp);
temp = 10;
console.log(temp += 5, temp);

// Increment expression pada for dapat menggunakan post increment, pre increment, ataupun compound assignment operator
for (let i = 0; i < 5; i++) {
  console.log(i);
}

for (let i = 0; i < 5; ++i) {
  console.log(i);
}

for (let i = 0; i < 10; i += 2) {
  console.log(i);
}
```

## Common Error
```javascript
// Kesalahan penentuan variable yang di-increment
let j = 0;
for (let i = 0; i < 10; j++) {
  console.log(i);
}

// Kesalahan menentukan operasi decrement atau increment
for (let i = 10; i > 0; i++) {
  console.log(i);
}
```

# Nested Iteration
```javascript
/**
 * REVIEW: ITERATION AND CONDITIONAL
 * 
 * Diberikan sebuah input kalimat dengan tipe string.
 * Buat sebuah program untuk mengubah kalimat tersebut ke dalam bentuk title case.
 * Contoh:
 *   Input: this is javascript
 *   Output: This Is Javascript
 */

let input = 'this is javascript';
let titleCase = input[0].toUpperCase();

for (let i = 1; i < input.length; i++) {
  if (input[i - 1] === ' ') {
    titleCase += input[i].toUpperCase();
  } else {
    titleCase += input[i];
  }
}

console.log(titleCase);

/**
 * Tampilkan angka 0 sampai 9 ke samping, sebanyak 5 kali.
 * Contoh:
 *   0123456789
 *   0123456789
 *   0123456789
 *   0123456789
 *   0123456789
 */

for (let i = 0; i < 5; i++) {
  let output = '';
  for (let j = 0; j < 10; j++) {
    output += j;
  }
  console.log(output);
}

/**
 * Diberikan sebuah input kata dengan tipe string.
 * Urutkan huruf yang ada dalam kata tersebut, sesuai dengan urutan alphabet.
 * Sebagai contoh:
 *   - Input  : jihgfedcba
 *     Output : abcdefghij
 *   - Input  : javascript
 *     Output : aacijprstv
 */

input = 'javascript';
let kamus = 'abcdefghijklmnopqrstuvwxyz';
let sorted = '';

// Implementasi pertama
for (let i = 0; i < kamus.length; i++) {
  for (let j = 0; j < input.length; j++) {
    if (kamus[i] === input[j]) {
      sorted += input[j];
    }
  }
}

// Implementasi kedua
for (let i = 0; i < kamus.length && sorted.length < input.length; i++) {
  for (let j = 0; j < input.length; j++) {
    if (kamus[i] === input[j]) {
      sorted += input[j];
    }
  }
}

console.log(sorted);

/**
 * Membuat built-in function indexOf() sederhana.
 * Apabila diberikan input kalimat dengan tipe string, buatlah sebuah program untuk mencari pada string tersebut terdapat sebuah penggalan kata.
 * Sebagai contoh:
 *   1. Input 1 : 'I love JavaScript'
 *      Input 2 : 'love'
 *      Output  : 2
 *   2. Input 1 : "This is programmer's live"
 *      Input 2 : 'hello'
 *      Output  : -1
 */

let input1 = 'I love JavaScript';
let input2 = 'love';
let count = 0;

for (let i = 0; i < input1.length; i++) {
  for (let j = 0; j < input2.length; j++) {
    if (input1[i + j] === input2[j]) {
      count++;
    } else {
      count = 0;
      break;
    }
  }
  if (count === input2.length) {
    console.log(i)
    break;
  }
}

if (count !== input2.length) {
  console.log(-1);
}
```

# Review: Conditional and Iteration
```javascript
```

# Function
```javascript
```

# Array
```javascript
/**
 * Membuat array
 */

var numbers = [0, 1, 2, 3, 4];
var furnitures = ['Table', 'Chair', 'Cupboard', 'Couch'];
var animals = ['Tiger', 'Elephant', 'Rhinoceros', 'Girafe'];

/**
 * Properti length
 */

console.log(numbers, numbers.length);
console.log(furnitures, furnitures.length);
console.log(animals, animals.length);

/**
 * Mengakses element array
 */

console.log(numbers[0], numbers[1], numbers[2], numbers[3], numbers[4]);
console.log(furnitures[0], furnitures[1], furnitures[2], furnitures[3]);
console.log(animals[0], animals[1], animals[2], animals[4]);

/**
 * Mengakses element array dengan looping
 */

for (var i = 0; i < numbers.length; i++) {
  console.log(numbers[i]);
}

for (var i = 0; i < furnitures.length; i++) {
  console.log(furnitures[i]);
}

for (var i = 0; i < animals.length; i++) {
  console.log(animals[i]);
}

/**
 * Menambahkan element baru ke array
 */

numbers.push(5);
furnitures.push('Television');
animals.push('Lion');

console.log(numbers);
console.log(furnitures);
console.log(animals);
```

```javascript
/**
 * Cari element terbesar dari sebuah array of numbers
 */

var numbers = [51, 4, 78, 22, 83, 100, 52];
var largest = 0;

for (var i = 0; i < numbers.length; i++) {
  if (largest < numbers[i]) {
    largest = numbers[i];
  }
}

console.log(largest)

/**
 * Cari element terkecil dari sebuah array of numbers
 */

var numbers = [51, 4, 78, 22, 83, 100, 52];
var smallest = numbers[0];

for (var i = 1; i < numbers.length; i++) {
  if (smallest > numbers[i]) {
    smallest = numbers[i];
  }
}

console.log(smallest)
```

```javascript
/**
 * Balik urutan array of numbers
 */

var numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];
var flippedNums = []
for (var i = numbers.length - 1; i > 0; i--) {
  flippedNums.push(numbers[i]);
}
console.log(flippedNums);
```

```javascript
/**
 * Bubble sort
 */

var numbers = [51, 4, 78, 22, 83, 100, 52];

for (var i = 0; i < numbers.length; i++) {
  for (var j = 0; j < numbers.length - 1; j++) {
    if (numbers[j] > numbers[j + 1]) {
      var temp = numbers[j];
      numbers[j] = numbers[j + 1];
      numbers[j + 1] = temp;
    }
  }
}

console.log(numbers);

/**
 * Optimasi bubble sort dengan flag
 */

var numbers = [51, 4, 78, 22, 83, 100, 52];

for (var i = 0; i < numbers.length; i++) {
  var swapped = false;
  for (var j = 0; j < numbers.length - 1; j++) {
    if (numbers[j] > numbers[j + 1]) {
      var temp = numbers[j];
      numbers[j] = numbers[j + 1];
      numbers[j + 1] = temp;
      swapped = true;
    }
  }
  if (swapped === false) {
    break;
  }
}

console.log(numbers);
```

```javascript
/**
 * String vs. Array
 * Unmutable vs. Mutable
 */

var string = '0123456789';
var array = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9'];

console.log(`string: ${string}`, `array: ${array}`);

string[0] = 'A';
array[0] = 'A';

console.log(`string: ${string}`, `array: ${array}`);
```

```javascript
/**
 * Sifat pass by reference para array
 */

let a = [1, 2, 3];
let b = a;

a[0] = 10;
console.log(a, b);
```

# Review: Array
```javascript
```

# Multidimensional Array
```javascript
```

# Review: Function, Array and Multidimensional Array
```javascript
/**
 * Review Function
 *   1. DRY and Reusability.
 *   2. Maintainability and Testing.
 *   3. Personal Safety.
 */


/** 1. DRY and Reusability **/

//// Not using function
let input = 'Hello   my     name      is       Acong';
let output = '';
for (let i = 0; i < input.length; i++) {
  output += input[i];
  while (input[i] === ' ' && input[i + 1] === ' ') {
    i++;
  }
}
console.log(output);

input = 'Nice   to meet   you,     my Name    is Sitorus';
output = '';
for (let i = 0; i < input.length; i++) {
  output += input[i];
  while (input[i] === ' ' && input[i + 1] === ' ') {
    i++;
  }
}
console.log(output);

//// Using function
function removeDupesSpace(sInput) {
  sOutput = '';
  for (let i = 0; i < sInput.length; i++) {
    sOutput += sInput[i];
    while (sInput[i] === ' ' && sInput[i + 1] === ' ') {
      i++;
    }
  }
  return sOutput;
}

console.log(removeDupesSpace('Hello   my     name      is       Acong'));
console.log(removeDupesSpace('Nice   to meet   you,     my Name    is Sitorus'));


/** 2. Maintainability and Testing **/

//// Not using function
input = 'Hello   my     name      is       Acong';
output = '';
for (let i = 0; i < input.length; i++) {
  output += input[i];
  while (input[i] === ' ' && input[i + 1] === ' ') {
    i++;
  }
}
console.log(output);

input = 'Nice   to meet   you,     my Name    is Sitorus';
output = '';
for (let i = 0; i < input.length; i++) {
  output += input[i];
  while (input[i] === ' ') { // Error in copy-pasting
    i++;
  }
}
console.log(output);


/** 3. Personal Safety **/
/**
 * If you're not using functions, you will incur the wrath of the person who will maintain your code later.
 * This will results in flaming, mocking, rarely even vandalism.
 */
```

```javascript
/**
 * Review Array
 *   1. Indexing.
 *   2. Mutability: Array vs String.
 *   3. length property.
 *   4. Mostly used to group same meaning variables together.
 */


/** Indexing **/
let arr = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j'];
console.log(arr[0]); // a
console.log(arr[1]); // b
console.log(arr[2]); // c


/** Mutability: Array vs String. **/

let str = 'abcdefghij';
arr = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j'];

str[0] = 'z';
arr[0] = 'z';

console.log(str, arr)


/** length property **/

arr = ['Acong', 'Djoko', 'Sitorus', 'Budi', 'Didi Kempot']
console.log(arr.length); // 5
console.log(arr[arr.length]); // undefined, because indexing starts from 0

for (let i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}


/** Mostly used to group same meaning variables together **/

let names = ['Acong', 'Djoko', 'Sitorus', 'Budi'];
let classes = ['X', 'XII', 'XII', 'XI'];
let hobbies = ['Sleep', 'Eat', 'Reading', 'Coding'];
```

```javascript
/**
 * Review Multidimensional Array
 *   1. Indexing.
 */


/** Indexing **/

// Multidimensional array is array which elements are array
let arr = [
  ['a', 'b', 'c'],
  ['d', 'e', 'f'],
  ['g', 'h', 'i']
];
console.log(arr[0][0]); // a
console.log(arr[1][0]); // d
console.log(arr[2][0]); // g

arr = [
  [['a', 'b'], 'c'],
  [['d', 'e'], 'f'],
  [['g', 'h'], 'i']
];
console.log(arr[0][0]);    // [ 'a', 'b' ]
console.log(arr[0][0][0]); // a
console.log(arr[1][0]);    // [ 'd', 'e' ]
console.log(arr[1][0][0]); // d
console.log(arr[2][2]);    // undefined
```

```javascript
/**
 * Soal Latihan Review: Function, Array and Multidimensional Array
 * 
 * Diberikan sebuah playlist dalam bentuk multidimensional array.
 * Sebuah lagu di dalam playlist memiliki format sebagai berikut ['Penyanyi', 'Judul Lagu', 'Durasi (menit)'].
 * 
 * Contoh dari playlist tersebut adalah seperti di bawah ini:
 * let playlist = [
 *   ['Didi Kempot', 'Banyu Langit', 4],
 *   ['Nike Ardilla', 'Sandiwara Cinta', 4],
 *   ['Hetty Koes Endang', 'Cinta Putih', 3],
 *   ['Titiek Puspa', 'Kupu-Kupu Malam', 3],
 *   ['Ahmad Albar', 'Don\'t Spoil My Day', 5],
 *   ['Doel Sumbang', 'Awewe Sapi Daging', 2],
 *   ['Ebiet G. Ade', 'Berita Kepada Kawan', 6]
 * ];
 * 
 * Berdasarkan playlist tersebut, buatlah 5 buah function berikut:
 *   1. sortBySinger(input, ascending)
 *      Function ini akan melakukan sorting playlist berdasarkan 'Penyanyi'. Function ini akan menerima 2 parameter yaitu:
 *        - input: playlist dalam format seperti pada contoh di atas.
 *        - ascending: flag sorting dengan tipe boolean.
 *   2. sortByTitle(input, ascending)
 *      Function ini akan melakukan sorting playlist berdasarkan 'Judul Lagu'. Function ini akan menerima 2 parameter yaitu:
 *        - input: playlist dalam format seperti pada contoh di atas.
 *        - ascending: flag sorting dengan tipe boolean.
 *   3. sortByDuration(input, ascending)
 *      Function ini akan melakukan sorting playlist berdasarkan 'Durasi (menit)'. Function ini akan menerima 2 parameter yaitu:
 *        - input: playlist dalam format seperti pada contoh di atas.
 *        - ascending: flag sorting dengan tipe boolean.
 *   4. sortPlaylist(input, by, ascending)
 *      Function ini akan melakukan sorting playlist berdasarkan parameter by. Function ini akan menerima 3 parameter yaitu:
 *        - input: playlist dalam format seperti pada contoh di atas.
 *        - by: sebuah string yang hanya dapat diisi dengan 'singer', 'title', atau 'duration'.
 *        - ascending: flag sorting dengan tipe boolean.
 *   5. play(input, time)
 *      Function ini akan memberikan return value berupa multidimensional array, yang berisi lagu-lagu yang dapat dimainkan berdasarkan
 *      time yang dialokasikan. Lagu-lagu yang ada dalam playlist akan dimainkan dengan urutan dari atas ke bawah
 *      Apabila time tidak cukup untuk memainkan 1 lagu full, maka lagu tersebut akan batal dimainkan dan proses play akan berhenti.
 *      Apabila sampai akhir playlist masih ada sisa time, maka lagu akan dimainkan dari atas kembali.
 *      Function ini akan menerima 2 parameter yaitu:
 *        - input: playlist dalam format seperti pada contoh di atas.
 *        - time: waktu (menit) dengan tipe number.
 */

let playlist = [
  ['Didi Kempot', 'Banyu Langit', 4],
  ['Nike Ardilla', 'Sandiwara Cinta', 4],
  ['Hetty Koes Endang', 'Cinta Putih', 3],
  ['Titiek Puspa', 'Kupu-Kupu Malam', 3],
  ['Ahmad Albar', 'Don\'t Spoil My Day', 5],
  ['Doel Sumbang', 'Awewe Sapi Daging', 2],
  ['Ebiet G. Ade', 'Berita Kepada Kawan', 6]
];

function sortBySinger(input, ascending) {
  let a = 1, b = 0;
  if (ascending === true) {
    a = 0, b = 1;
  }

  for (let i = 0; i < input.length; i++) {
    let swapped = false;
    for (let j = 0; j < input.length - 1; j++) {
      if (input[j + a][0] > input[j + b][0]) {
        [input[j], input[j + 1]] = [input[j + 1], input[j]];
        swapped = true;
      }
    }
    if (swapped === false) {
      break;
    }
  }
}

function sortByTitle(input, ascending) {
  let a = 1, b = 0;
  if (ascending === true) {
    a = 0, b = 1;
  }

  for (let i = 0; i < input.length; i++) {
    let swapped = false;
    for (let j = 0; j < input.length - 1; j++) {
      if (input[j + a][1] > input[j + b][1]) {
        [input[j], input[j + 1]] = [input[j + 1], input[j]];
        swapped = true;
      }
    }
    if (swapped === false) {
      break;
    }
  }
}

function sortByDuration(input, ascending) {
  let a = 1, b = 0;
  if (ascending === true) {
    a = 0, b = 1;
  }

  for (let i = 0; i < input.length; i++) {
    let swapped = false;
    for (let j = 0; j < input.length - 1; j++) {
      if (input[j + a][2] > input[j + b][2]) {
        [input[j], input[j + 1]] = [input[j + 1], input[j]];
        swapped = true;
      }
    }
    if (swapped === false) {
      break;
    }
  }
}

function sortPlaylist(input, by, ascending) {
  let bySort = 0;
  switch (by) {
    case 'singer':
      bySort = 0;
      break;
    case 'title':
      bySort = 1;
      break;
    case 'duration':
      bySort = 2;
      break;
  }

  let a = 1, b = 0;
  if (ascending === true) {
    a = 0, b = 1;
  }

  for (let i = 0; i < input.length; i++) {
    let swapped = false;
    for (let j = 0; j < input.length - 1; j++) {
      if (input[j + a][bySort] > input[j + b][bySort]) {
        [input[j], input[j + 1]] = [input[j + 1], input[j]];
        swapped = true;
      }
    }
    if (swapped === false) {
      break;
    }
  }
}

function play(input, time) {
  let retVal = [];
  let index = 0;

  while (time >= input[index][2]) {
    retVal.push(input[index]);
    time -= input[index][2];
    index++;
    if (index === input.length) {
      index = 0;
    }
  }

  return retVal;
}

// Test case 1
console.log(play(playlist, 35))
/**
 * [
 *   [ 'Didi Kempot', 'Banyu Langit', 4 ],
 *   [ 'Nike Ardilla', 'Sandiwara Cinta', 4 ],
 *   [ 'Hetty Koes Endang', 'Cinta Putih', 3 ],
 *   [ 'Titiek Puspa', 'Kupu-Kupu Malam', 3 ],
 *   [ 'Ahmad Albar', "Don't Spoil My Day", 5 ],
 *   [ 'Doel Sumbang', 'Awewe Sapi Daging', 2 ],
 *   [ 'Ebiet G. Ade', 'Berita Kepada Kawan', 6 ],
 *   [ 'Didi Kempot', 'Banyu Langit', 4 ],
 *   [ 'Nike Ardilla', 'Sandiwara Cinta', 4 ]
 * ]
 */

// Test case 2
sortPlaylist(playlist, 'duration', true);
console.log(play(playlist, 35));
/**
 * [
 *   [ 'Doel Sumbang', 'Awewe Sapi Daging', 2 ],
 *   [ 'Hetty Koes Endang', 'Cinta Putih', 3 ],
 *   [ 'Titiek Puspa', 'Kupu-Kupu Malam', 3 ],
 *   [ 'Didi Kempot', 'Banyu Langit', 4 ],
 *   [ 'Nike Ardilla', 'Sandiwara Cinta', 4 ],
 *   [ 'Ahmad Albar', "Don't Spoil My Day", 5 ],
 *   [ 'Ebiet G. Ade', 'Berita Kepada Kawan', 6 ],
 *   [ 'Doel Sumbang', 'Awewe Sapi Daging', 2 ],
 *   [ 'Hetty Koes Endang', 'Cinta Putih', 3 ],
 *   [ 'Titiek Puspa', 'Kupu-Kupu Malam', 3 ]
 * ]
 */
```

# Modular Functions
```javascript
```

# Review: Up to Modular Functions
```javascript
/**
 * Intensive Care Unit Scoring
 *
 * Soal ini meminta kita untuk membuat sebuah program untuk mensimulasikan scoring ICU pada sebuah rumah sakit.
 * Pasien akan ditampung ke dalam sebuah array dengan format ['Nama Pasien', 'Symptoms', 'Umur', 'Tingkat Bahaya'].
 * Pasien-pasien tersebut akan ditampung ke dalam sebuah multidimensional array seperti di bawah:
 *
 * let patients = [
 *   ['Acong', 'Sesak nafas', 39, 'Critical'],
 *   ['Djoko', 'Encok', 60, 'Severe'],
 *   ['Sitorus', 'Patah tulang', 11, 'Bearable'],
 *   ['Ajeng', 'Kena pisau waktu memasak', 43, 'Minor'],
 *   ['Dhani', 'Diare', 28, 'Bearable'],
 *   ['Abdhul', 'Perut mual', 18, 'Severe'],
 *   ['Conor McGregor', 'Bengkak di leher', 31, 'Severe'],
 *   ['Cristiano Ronaldo', 'Bengkak di kaki', 35, 'Bearable'],
 *   ['Rama', 'Hati', 21, 'Critical'],
 *   ['Shinta', 'Hati', 21, 'Minor'],
 *   ['Bahamut', 'Sariawan', 90, 'Minor'],
 *   ['Tiamat', 'Pandangan kabur', 80, 'Critical'],
 *   ['Cthulu', 'Kepala benjol', 26, 'Minor'],
 *   ['Han Solo', 'Luka tembak', 38, 'Critical']
 * ]
 *
 * Masing-masing 'Tingkat Bahaya' memiliki bobot sebagai berikut:
 *   - 'Critical' : 4
 *   - 'Severe'   : 3
 *   - 'Bearable' : 2
 *   - 'Minor'    : 1
 *
 * Scoring akan dilakukan berdasarkan 'Umur' dan 'Tingkat Bahaya' dengan perhitungan sebagai berikut:
 *   'Score' = 'Umur' / 100  + 'Tingkat Bahaya'
 *
 * Buatlah program yang akan memberikan return value berupa multidimensional array yang berisi urutan-urutan pasien yang akan ditangani, berdasarkan 'Score' tertinggi ke 'Score' terendah.
 * Selesaikan permasalahan ini dengan modular functions
 */

/**
 * Function ini akan melakukan konversi dari string 'Tingkat Bahaya' ke nilai angka padanannya.
 * Return value dari function ini adalah representasi angka dari 'Tingkat Bahaya'.
 */
function dangerScale(input) {
  switch (input) {
    case 'Critical':
      return 4;
    case 'Severe':
      return 3;
    case 'Bearable':
      return 2;
    case 'Minor':
      return 1;
  }
}

// console.log(dangerScale('Critical'));  // 4
// console.log(dangerScale('Severe'));    // 3
// console.log(dangerScale('Bearable'));  // 2
// console.log(dangerScale('Minor'));     // 1

/**
 * Function ini akan menerima array patient yang akan dihitung 'Score'-nya.
 * Return value dari function ini adalah score yang telah dihitung berdasarkan:
 *   - Representasi angka dari 'Tingkat Bahaya'
 *   - Umur
 * 
 * Formula perhitungan yang digunakan adalah:
 *   'Score' = 'Umur' / 100  + 'Tingkat Bahaya'
 */
function calculateScore(input) {
  return input[2] / 100 + dangerScale(input[3]);
}

// console.log(calculateScore(['Acong', 'Sesak nafas', 39, 'Critical']));     // 4.39
// console.log(calculateScore(['Djoko', 'Encok', 60, 'Severe']));             // 3.6
// console.log(calculateScore(['Sitorus', 'Patah tulang', 11, 'Bearable']));  // 2.11
// console.log(calculateScore(['Han Solo', 'Luka tembak', 38, 'Critical']));  // 4.38

/**
 * Function ini akan menerima array patient.
 * Return value dari function ini adalah array patient yang sudah ditambahi dengan 'Score'.
 */
function appendScore(input) {
  input.push(calculateScore(input));
  return input;
}

// console.log(appendScore(['Acong', 'Sesak nafas', 39, 'Critical']));     // [ 'Acong', 'Sesak nafas', 39, 'Critical', 4.39 ]
// console.log(appendScore(['Djoko', 'Encok', 60, 'Severe']));             // [ 'Djoko', 'Encok', 60, 'Severe', 3.6 ]
// console.log(appendScore(['Sitorus', 'Patah tulang', 11, 'Bearable']));  // [ 'Sitorus', 'Patah tulang', 11, 'Bearable', 2.11 ]
// console.log(appendScore(['Han Solo', 'Luka tembak', 38, 'Critical']));  // [ 'Han Solo', 'Luka tembak', 38, 'Critical', 4.38 ]

/**
 * Function ini akan menerima multidimensional array, yaitu list para pasien.
 * Return value dari function ini adalah list para pasien yang telah diurutkan berdasarkan 'Score' (descending).
 */
function icuPatientPriority(input) {
  for (let i = 0; i < input.length; i++) {
    input[i] = appendScore(input[i]);
  }

  for (let i = 0; i < input.length; i++) {
    let swapped = false;
    for (let j = 0; j < input.length - 1; j++) {
      if (input[j][4] < input[j + 1][4]) {
        [input[j], input[j + 1]] = [input[j + 1], input[j]];
        swapped = true;
      }
    }
    if (swapped === false) {
      break;
    }
  }
}

let patients = [
  ['Acong', 'Sesak nafas', 39, 'Critical'],
  ['Djoko', 'Encok', 60, 'Severe'],
  ['Sitorus', 'Patah tulang', 11, 'Bearable'],
  ['Ajeng', 'Kena pisau waktu memasak', 43, 'Minor'],
  ['Dhani', 'Diare', 28, 'Bearable'],
  ['Abdhul', 'Perut mual', 18, 'Severe'],
  ['Conor McGregor', 'Bengkak di leher', 31, 'Severe'],
  ['Cristiano Ronaldo', 'Bengkak di kaki', 35, 'Bearable'],
  ['Rama', 'Hati', 21, 'Critical'],
  ['Shinta', 'Hati', 21, 'Minor'],
  ['Bahamut', 'Sariawan', 90, 'Minor'],
  ['Tiamat', 'Pandangan kabur', 80, 'Critical'],
  ['Cthulu', 'Kepala benjol', 26, 'Minor'],
  ['Han Solo', 'Luka tembak', 38, 'Critical']
];

icuPatientPriority(patients)
console.log(patients);
// [
//   [ 'Tiamat', 'Pandangan kabur', 80, 'Critical', 4.8 ],
//   [ 'Acong', 'Sesak nafas', 39, 'Critical', 4.39 ],
//   [ 'Han Solo', 'Luka tembak', 38, 'Critical', 4.38 ],
//   [ 'Rama', 'Hati', 21, 'Critical', 4.21 ],
//   [ 'Djoko', 'Encok', 60, 'Severe', 3.6 ],
//   [ 'Conor McGregor', 'Bengkak di leher', 31, 'Severe', 3.31 ],
//   [ 'Abdhul', 'Perut mual', 18, 'Severe', 3.18 ],
//   [ 'Cristiano Ronaldo', 'Bengkak di kaki', 35, 'Bearable', 2.35 ],
//   [ 'Dhani', 'Diare', 28, 'Bearable', 2.2800000000000002 ],
//   [ 'Sitorus', 'Patah tulang', 11, 'Bearable', 2.11 ],
//   [ 'Bahamut', 'Sariawan', 90, 'Minor', 1.9 ],
//   [ 'Ajeng', 'Kena pisau waktu memasak', 43, 'Minor', 1.43 ],
//   [ 'Cthulu', 'Kepala benjol', 26, 'Minor', 1.26 ],
//   [ 'Shinta', 'Hati', 21, 'Minor', 1.21 ]
// ]
```

# Object Literal
[Object Literal](./assets/object-literal.pdf)

```javascript
/**
 * Buat key baru yaitu sellPrice pada product, dengan value:
 *   sellPrice = (price + (price * profit / 100))
 */

let profit = 10;

let product = {
  name: 'Baygon',
  form: 'Aerosol',
  bugType: 'Roaces',
  price: 15000
};

// Do something here

console.log(product);
// {
//   name: 'Baygon',
//   form: 'Aerosol',
//   bugType: 'Roaces',
//   price: 15000,
//   sellPrice: 16500
// }
```

```javascript
/**
 * Tampilkan semua value yang terdapat pada object sensebounce ke bawah,
 * termasuk isi key colors dan key warehouseStock.
 */

let sensebounce = {
  name: 'Sensebounce+ SUMMER.RDY Shoes',
  manufacturer: 'Adidas',
  gender: 'Men',
  sport: 'Running',
  weightGram: 366,
  colors: ['Black', 'White'],
  warehouseStock: {
    warehouse1: 0,
    warehouse2: 10,
    warehouse3: 2
  }
};

// Do something here

// Sensebounce+ SUMMER.RDY Shoes
// Adidas
// Men
// Running
// 366
// Black
// White
// 0
// 10
// 2
```

```javascript
/**
 * Buat sebuah function untuk memeriksa apakah dua buah object literal sama atau tidak.
 * Function tersebut akan memberikan return value true jika sama,
 * dan return value false jika tidak sama.
 */

let a = { key1: 'A', key2: 10, key3: true };
let b = { key1: 'A', key2: 10, key3: true };
let c = { key1: 11, key2: 'B', key3: true };

function isObjLiteralEqual(inObj1, inObj2) {
  // Do something here
}

console.log(isObjLiteralEqual(a, b)); // true
console.log(isObjLiteralEqual(a, c)); // false
```

```javascript
/**
 * Terdapat sebuah list pasien yang berisi nama serta gejala yang dialami.
 * Buatlah sebuah fungsi untuk mengelompokkan pasien-pasien berdasarkan gejalanya.
 * Hasil yang diharapkan dari pengelompokan tersebut adalah sebuah object.
 * Perhatikan test case yang diberikan.
 */

let patients = [
  ['Acong', 'Mual'],
  ['Djoko', 'Pusing'],
  ['Sitorus', 'Batuk'],
  ['Rama', 'Pusing'],
  ['Shinta', 'Batuk'],
  ['Cthulu', 'Mual'],
  ['Nyarlothep', 'Mual'],
];

// Do something here

// {
//   Mual: [ 'Acong', 'Cthulu', 'Nyarlothep' ],
//   Pusing: [ 'Djoko', 'Rama' ],
//   Batuk: [ 'Sitorus', 'Shinta' ]
// }
```

# Array of Object
```javascript
// Review Object

/**
 * Membuat object literal cara 1
 */

var karyawan1 = {
  nama: 'Budi',
  profesi: 'Pilot',
  asal: 'Pekanbaru',
  umur: 8,
  bukuFav: ['How to Fly Airplane for Dummies', 'Basic of Aerodymics'],
  adik: {
    nama: 'Acong',
    profesi: 'Pelajar'
  }
};
console.log('karyawan1:', karyawan1);
console.log('--------------------------------------------');

/**
 * Membuat object literal cara 2
 */

var karyawan2 = {};
karyawan2.nama = 'Budi';
karyawan2.profesi = 'Pilot';
var temp = 'asal';
karyawan2[temp] = 'Pekanbaru';
console.log('karyawan2:', karyawan2);
console.log('--------------------------------------------');


/**
 * Mengakses value dari object
 */

console.log('Pengaksesan value dari object:');
for (var key in karyawan1) { // Untuk semua key yang terdapat pada objeckaryawan1, lakukan statement yang ada di dalam for
  if (key === 'bukuFav') {
    for (var i = 0; i < karyawan1[key].length; i++) {
      console.log(karyawan1[key][i])
    }
  } else {
    console.log(karyawan1[key]);
  }
}
console.log('--------------------------------------------');
```

```javascript
/**
 * Ubah multidimensional array di bawah ke dalam bentuk array of object.
 * Array elemen ke [x][0] akan ditampung ke dalam key 'nama'.
 * Array elemen ke [x][1] akan ditampung ke dalam key 'hobi'.
 */

var arr = [
  ['Acong', 'Main Bola'],
  ['Djoko', 'Belajar'],
  ['Sitorus', 'Makan']
];

var retVal = [];

for (var i = 0; i < arr.length; i++) {
  var temp = {};
  temp.nama = arr[i][0];
  temp.hobi = arr[i][1];
  retVal.push(temp);
}

console.log(retVal);
```

```javascript
/**
 * Buatlah sebuah fungsi yang akan memberikan sebuah array of object yang berisi
 * produk obat apa saja yang bisa dibeli dengan jumlah uang yang diberikan.
 */

var database = [
  {
    nama: 'Oskadon',
    harga: 5000
  },
  {
    nama: 'Komix',
    harga: 3500
  },
  {
    nama: 'OBH Combi Plus',
    harga: 25000
  },
  {
    nama: 'Koyo Cabe',
    harga: 15000
  },
  {
    nama: 'Panadol',
    harga: 17000
  }
];

function buyableGoods(db, money) {
  var retVal = [];
  for (var i = 0; i < db.length; i++) {
    if (db[i].harga <= money) {
      retVal.push(db[i]);
    }
  }
  return retVal;
}

console.log(buyableGoods(database, 17000));
// [
//   { nama: 'Oskadon', harga: 5000 },
//   { nama: 'Komix', harga: 3500 },
//   { nama: 'Koyo Cabe', harga: 15000 }
// ]

console.log(buyableGoods(database, 2000));
// []

console.log(buyableGoods(database, 10000));
// [
//   { nama: 'Oskadon', harga: 5000 },
//   { nama: 'Komix', harga: 3500 }
// ]
```

```javascript
/**
 * Seorang pedagang susu keliling hendak menjual barang dagangannya.
 * Penjualan akan diprioritaskan untuk susu yang akan kadaluarsa terlebih dahulu.
 * Susu-susu dagangan akan diwakilkan dengan sebuah array of objects.
 * Buatlah sebuah fungsi dengan output sesuai contoh test case yang diberikan.
 */

var database = [
  { name: 'Indomilk', id: 'IDM-001', daysBeforeExp: 10 },
  { name: 'Ultramilk', id: 'UTM-001', daysBeforeExp: 3 },
  { name: 'Indomilk', id: 'IDM-002', daysBeforeExp: 15 },
  { name: 'Ultramilk', id: 'UTM-002', daysBeforeExp: 1 },
  { name: 'Indomilk', id: 'IDM-003', daysBeforeExp: 5 },
  { name: 'Ultramilk', id: 'UTM-003', daysBeforeExp: 8 },
  { name: 'Bendera', id: 'BDR-001', daysBeforeExp: 5 }
];

function firstToSell(db) {
  var retVal = {};
  for (var i = 0; i < db.length; i++) {
    for (var j = 0; j < db.length - 1; j++) {
      if (db[j].daysBeforeExp > db[j + 1].daysBeforeExp) {
        var temp = db[j];
        db[j] = db[j + 1];
        db[j + 1] = temp;
      }
    }
  }
  for (var i = 0; i < db.length; i++) {
    if (!(db[i].name in retVal)) { // Jika db[i].name itu tidak terdapat di dalam object retVal sebagai key, lakukan yang ada di dalam if
      retVal[db[i].name] = [];
    }
    retVal[db[i].name].push(db[i]);
  }
  return retVal;
}

console.log(firstToSell(database));
// {
//   Ultramilk: [
//     { name: 'Ultramilk', id: 'UTM-002', daysBeforeExp: 1 },
//     { name: 'Ultramilk', id: 'UTM-001', daysBeforeExp: 3 },
//     { name: 'Ultramilk', id: 'UTM-003', daysBeforeExp: 8 }
//   ],
//   Indomilk: [
//     { name: 'Indomilk', id: 'IDM-003', daysBeforeExp: 5 },
//     { name: 'Indomilk', id: 'IDM-001', daysBeforeExp: 10 },
//     { name: 'Indomilk', id: 'IDM-002', daysBeforeExp: 15 }
//   ],
//   Bendera: [ { name: 'Bendera', id: 'BDR-001', daysBeforeExp: 5 } ]
// }
```

```javascript
/**
 * Untuk mensimulasikan database obat, kita akan menggunakan array yang berisi object obat.
 * Sebuah object obat memiliki contoh susunan sebagai berikut:
 * var oskadon = {
 *   nama: 'Oskadon',
 *   untuk: ['Sakit kepala', 'Hidung tersumbat', 'Pegal-pegal'],
 *   harga: 5000
 * }
 * 
 * Berdasarkan database obat yang ada, buatlah sebuah fungsi yang akan
 * memberikan saran obat apa saja yang cocok untuk penyakit dari konsumen.
 */

var database = [
  {
    nama: 'Oskadon',
    untuk: ['Sakit kepala', 'Hidung tersumbat', 'Pegal-pegal'],
    harga: 5000
  }, {
    nama: 'Komix',
    untuk: ['Sakit tenggorokan', 'Batuk berdahak', 'Batuk tidak berdahak'],
    harga: 3500
  }, {
    nama: 'OBH Combi Plus',
    untuk: ['Batuk berdahak', 'Batuk tidak berdahak'],
    harga: 25000
  }, {
    nama: 'Koyo Cabe',
    untuk: ['Nyeri pinggang', 'Pegal-pegal'],
    harga: 15000
  }
];

function getSuitableMedicine(db, symptom) {
  var retVal = [];
  for (var i = 0; i < db.length; i++) {
    for (var j = 0; j < db[i].untuk.length; j++) {
      if (db[i].untuk[j] === symptom) {
        retVal.push(db[i]);
      }
    }
  }
  return retVal;
}

console.log(getSuitableMedicine(database, 'Pegal-pegal'));
// [
//   {
//     nama: 'Oskadon',
//     untuk: [ 'Sakit kepala', 'Hidung tersumbat', 'Pegal-pegal' ],
//     harga: 5000
//   },
//   {
//     nama: 'Koyo Cabe',
//     untuk: [ 'Nyeri pinggang', 'Pegal-pegal' ],
//     harga: 15000
//   }
// ]

console.log(getSuitableMedicine(database, 'Batuk berdahak'));
// [
//   {
//     nama: 'Komix',
//     untuk: [ 'Sakit tenggorokan', 'Batuk berdahak', 'Batuk tidaberdahak' ],
//     harga: 3500
//   },
//   {
//     nama: 'OBH Combi Plus',
//     untuk: [ 'Batuk berdahak', 'Batuk tidak berdahak' ],
//     harga: 25000
//   }
// ]

console.log(getSuitableMedicine(database, 'Nyeri pinggang'));
// [
//   {
//     nama: 'Koyo Cabe',
//     untuk: [ 'Nyeri pinggang', 'Pegal-pegal' ],
//     harga: 15000
//   }
// ]
```

```javascript
/**
 * Contoh pass by reference
 */

var a = [1, 2, 3];
var b = a; // Kita menyamakan alamat dari b dengan a
console.log(b);
a[0] = 5;
console.log(b);

var objA = {
  nilai: 10
}
var objB = objA;  // Kita menyamakan alamat dari b dengan a
console.log(objB);
objA.nilai = 9;
console.log(objB);
```

# Tracing and Debugging
Tracing and Debugging adalah proses untuk menemukan bagian code mana yang error untuk kemudian diperbaiki. Secara sederhana, proses ini dilakukan dengan memperhatikan syntax, proses, variable serta perubahan nilai secara perlahan lahan

Umumnya terdapat tiga bentuk error: 
- 🐞️ Syntax error: program tidak dapat dieksekusi.
- 🐞️ Runtime error: error yang terjadi ketika program dieksekusi. Umumnya output yang diberikan tidak sesuai, atau crash.
- 🐞️ Logic error:  program memberikan output yang tidak diharapkan.

## Syntax Error
Syntax error dapat dideteksi oleh code editor (misal: VSCode). Biasanya error ini akan memberikan tanda garis zig-zag merah di teks. Beberapa contoh sumber syntax error:
- Penulisan nama variabel yang salah seperti:
  ```javascript
  let 3orangSaja = ['Acong', 'Djoko', 'Sitorus'];
  ```
  ```javascript
  let #HelloWorld = '#HelloWorld';
  ```
- Kurang pembuka atau penutup parenthesis:
  ```javascript
  for (let i = 0; i < 5; i++
  ```
- Lupa menggunakan koma para array atau object literal seperti:
  ```javascript
  let angkaKu = [1, 2 3];
  ```
  ```javascript
  let objectKu = { key1: 'Hello' key2: 'World' };
  ```
- Copy-paste memberikan format yang berbeda, misal dari slack ke VSCode.
- Lupa melakukan comment / penutup comment
  ```javascript
  let string = 'Hacktiv8 - Amsterdam Fox'

  function reverseString(str) {
    let ret = '';
    for (let i = str.length - 1; i >= 0; i--) {
      ret += str[i];
    }
    return ret;
  }
  console.log(reverseString);
      
  /** Fungsi ini digunakan untuk membalik string
  ```
### 🔎️🐞️🔨️ How to Avoid Syntax Error:
- Periksa apakah terdapat garis zig-zag merah di code editor.
- Sebelum pindah ke baris berikutnya, periksa apakah syntax pada baris itu sudah sesuai.
- Selalu hati-hati dengan proses copy-paste kode program, karena bisa saja format yang dihasilkan tidak sama.
- Perbaiki indentasi agar scope kode program terlihat dengan jelas.
- Sebelum dianggap selesai, coba cek dari baris pertama sampai terakhir file.
- Gunakan `"use strict"` (menggunakan DOUBLE QUOTES). [Referensi](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode).


## Runtime Error
Runtime error tidak terdeteksi di code editor, namun terdeteksi ketika program dieksekusi. Saat proses eksekusi, biasanya akan diinformasikan jenis error-nya dan lokasi baris dimana error terjadi. Beberapa contoh sumber runtime error:
- Deklarasi ulang variable.
  ```javascript
  let variableku = 10;
  let variableku = 20;
  ```
- Variabel belum dideklarasikan atau salah menulis pengejaan variabel.
  ```javascript
  let uvuvwevwe = 10;
  console.log(uvuvwewve);
  ```
- Memanggil variabel pada scope yang salah.
  ```javascript
  let variable1 = 5;

  for (let i = 0; i < 10; i++) {
    console.log('alert');
    if (i > variable1) {
      break;
    }
  }
  
  console.log(`Berhenti pada waktu nilai i = ${i}`);
  ```
- Memanggil built-in function yang tidak ada di JavaScript.
  ```javascript
  let array = [5, 3, 2, 7, 1];
  console.log(array.Sort());
  ```
  ```javascript
  console.log(isNan(15));
  ```
- Infinite Loop.
  ```javascript
  let string = 'Hacktiv8 - Amsterdam Fox'

  function reverseString(str) {
    let ret = '';
    for (let i = str.length - 1; i >= 0; i++) {
      ret += str[i];
    }
    return ret;
  }

  console.log(reverseString(string));
  ```
- Menggunakan properti atau built-in function yang tidak sesuai untuk tipe data tertentu.
  ```javascript
  let array = [1, 2, 3, 4, 5];

  for (let i = array.length; i > 0; i--) {
    console.log(array[i].toString());
  }
  ```

### 🔎️🐞️🔨️ How to Avoid Runtime Error
- Baca dan mengerti error yang ditampilkan, biasanya yang paling relevan terdapat pada baris atas. Apabila tidak mengerti apa yang dimaksudkan, lakukan searching pada Google dengan cara copy-paste informasi paling general dari pesan error.
- Ketika tidak terdapat tampilan pada terminal, atau terminal seolah berhenti pada suatu proses, maka kemungkinan besar terjadi infinite loop. Periksa penulisan loop, jika perlu gunakan `console.log()` untuk menampilkan variable looping.
- Tracing Kode kalian apalagi saat berhubungan dengan loop dan array untuk setiap variabel yang berpotensi berubah value-nya.
- Gunakan `typeof` karena kemungkinan test-case menggunakan tipe data yang berbeda.

## Semantic Error
Semantic error tidak terdeteksi oleh code editor dan terminal. Error ini menyebabkan program memberikan hasil output yang tidak kita harapkan. Semantic error terjadi jika terdapat kesalahan alur logic pada kode program. Contoh semantic error:
```javascript
let kapasitas = 5;
let sisa = 4.5;

let persentase = sisa / kapasitas;
console.log(`Sisa bensin: ${persentase} persen`);
```

### 🔎️🐞️🔨️ How to Avoid Semantic Error
- Buat algoritma sebelum membuat kode program. Algoritma ditujukan untuk membuat kerangka kerja program. Hal tersebut akan membantu kita dalam membuat kode program yang sudah jelas akan melakukan apa pada setiap step-nya.
- Gunakan `console.log()` untuk proses debug.
- Perbanyak latihan.
- Lakukan penamaan variabel sesuai dengan fungsi atau proses yang diwakili. Jangan melakukan hal berikut:
  ```javascript
  for (let terserahDeh = 0; terserahDeh < 10; terserahDeh++) {
    console.log(terserahDeh);
  }
  ```

## Misc. Notes
- Inisialisasi variabel di dalam looping maka akan inisialisasi ulang setiap loop dan mereset nilainya dan dianggap variabel baru. Ini hanya berguna untuk temp dalam 1 loop misalnya ditampung oleh variabel lain. (Bisa menyebabkan infinite loop).
- Maka harus dipikirkan apakah variabel harus di inisialisasi ulang ditaruh di dalam loop atau diluar.
- Indentasi kurang rapi, menyulitkan untuk membaca koding itu lagi dan menyulitkan jika ada syntax yang salah.
- Baca penggunaan built-in function sebelum diterapkan ke soal, kadang menggunakan asumsi ternyata penggunaan built-in yang kita pakai salah (Contoh: Math.random() , perbedaan splice dan slice).
- Jangan gunakan kode yang di soal tersebut tidak jadi digunakan/tidak perlu.
- Pahami maksud soal terlebih dahulu, hindari langsung kerjakan.
- Tidak membaca rules / restriction pada soal dan perhatikan apakah soal harus membutuhkan Pseudocode.
- Gambarkan secara visual atau pakai analogi di kertas saat mengerjakan soal yang sulit di pahami.
- Jangan jadi requirement-boy, ketika sudah sesuai testcase dan masih ada waktu langsung puas. Modif testcase sampai program menjadi general.
- Cek di dalam IF apakah itu operator comparison atau assignment (== atau =). Seharusnya comparison.
- Jika membutuhkan sesuatu yang tidak dipengaruhi loop (index i atau j, dsb..), maka buatlah counter tambahan diluar loop.
- Modulus bukan berarti pembagian, tapi pengurangan dengan operand terus menerus. Jika tidak bisa lagi dikurangi dengan operand, maka itulah nilai modulus.
- Modulus jika angka yang dimodulus lebih kecil dari operand, maka nilai modulus adalah angka yg dimodulus tersebut.
- Else digunakan untuk menangkap kondisi kondisi yang terlewat dari prediksi kita, Kadang kita juga tidak perlu menggunakan dalam kasus kasus tertentu. Misal toggling ketika operasi memang harus berjalan atau tidak ketika tidak valid.
- Jika ingin menuliskan algoritma gunakan bahasa yang deskriptif seperti kita menjelaskan sebuah cara penyelesaian ke orang umum/teman.
- Jika ingin menuliskan pseudocode gunakan bahasa yang mewakili proses penyelesaian dan deskriptif tapi pendekatannya lebih ke coding tapi general bisa diterapkan ke semua bahasa pemrograman. Indentasi di pseudocode menunjukkan blok kode. Mengacu ke materi hacktiv8 dan link pseudocode standart.
- Ketika mengumpulkan tugas, tidak perlu menampilkan output proses yang tidak perlu (contoh console.log nilai semetara didalam looping, karena yang dibutuhkan hanya hasil akhir).
- Jika ingin challenge tambahan, coba ubah-ubah soal challenge misal dari salah satu argument berupa 1 string menjadi array berisi banyak string.
- Hindari penggunakan built-in function untuk kasus yang sederhana. Jika perlu buatlah 2 jawaban yang pakai built-in dan yang tidak pakai built-in.
- Jika sudah selesai mengerjakan tugas, hapus variabel-variabel yang tidak terpakai dan output yang tidak digunaan.
- Perhatikan setiap testcase apakah ada validasi jika tidak ada argument, nilai string kosong, array kosong. Umumnya validasi bisa dikerjakan di awal di taruh dalam kondisi dan langsung diberikan return agar tidak mengerjakan baris program dari nilai argumen yang lolos validasi.
- Refactor ulang kode jika perlu, untuk menyederhanakan proses.
- Hindari hardcode agar kode bisa general menerima semua bentuk input. Umumnya hardcode terjadi ketika bingung limit/end dari loop.
- Selalu gunakan deklarasi jangan hanya nama variabel dan langsung tentukan tipedata dengan mengisi nilai default-nya untuk menghindari hasil proses yang undefined.
- Jangan lupa jika yang ingin di iterasi adalah array, selalu gunakan length.
- Penempatan return diluar function tidak mempunyai meaning/tidak berguna. Return hanya berkerja di dalam function.
- Penempatan return di dalam loop akan menghentikan proses yang ada di loop, jadi berhati hati. Bisa digunakan untuk pengganti break saat di dalam kondisi.
- Perhatikan length dari array jika dia length nya genap atau ganjil. Jika ganjil length-nya dibagi 2 maka akan ada angka desimal. Jika mengakses item dengan index desimal (misal arr[2.5]) maka akan undefined.
- Explore tentang teknik flagging menggunakan variabel yang di set true/false ketika masuk kondisi tertentu.
- Jangan copy-paste kode dari internet jika tidak tahu maksud kode tersebut.
- Biasakan penamaan variabel menggunakan bahasa inggris (era global, agar mudah dipahami dan bisa dibaca semua orang tanpa batasan bahasa).
- Biasakan penamaan variabel dengan camelCase dan jika seperti array itu plural (jamak) agar menunjukkan kalau dia bisa berisi lebih dari 1 nilai / list. Misal: listNumbers, numbers, animals, arrAnimals, dsb.

## References

### Stack Trace => Native Error Types:
- http://www.ecma-international.org/ecma-262/6.0/#sec-native-error-types-used-in-this-standard
- https://harrymoreno.com/2017/02/25/how-to-read-a-javascript-stack-trace.html
- http://www.ecma-international.org/ecma-262/6.0/#sec-undefined-value

### Tracing Practice (Array and Loop):
- https://www.101computing.net/using-trace-tables/

### Coding Style:
- https://javascript.info/coding-style
- https://github.com/airbnb/javascript

 ### Algorithm Patterns:
- https://medium.com/future-vision/problem-solving-patterns-programming-eebdb8eb24e0
- https://hackernoon.com/14-patterns-to-ace-any-coding-interview-question-c5bb3357f6ed
- https://smootok.com/problem-solving-pattern-in-programming/

### Problem Solving Steps:
- https://codeburst.io/10-steps-to-solving-a-programming-problem-8a32d1e96d74
- https://smootok.com/problem-solving-approach-in-programming/
- https://www.freecodecamp.org/news/how-to-think-like-a-programmer-lessons-in-problem-solving-d1d8bf1de7d2/

# Review: All
```javascript
```

# Local Git
[Local Git]([Terminal](./assets/terminal-git-and-github.pdf))

# Git Branch, Git Merge, GitHub Pull Request and GitHub.io
[Branch, Merge and Pull Request](./assets/branch-merge-pull-request.pdf)