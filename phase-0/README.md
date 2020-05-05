# Terminal, Git, and GitHub
[Google Slides - Terminal, Git and GitHub](https://docs.google.com/presentation/d/1tmbfRBavbf8h6IaXc23RWPYCSAH2jbVdrAMwa4Js0uE/edit?usp=drivesdk)

# HTML
```html
```

# CSS
```css
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
[Google Slides - Iteration in Pseudocode and JavaScript](https://docs.google.com/presentation/d/1ImOcY0pNTRCKFbpa0LFOTC2zMueOFasFv2XhejahI6c/edit?usp=sharing)


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
for (let i = 0; i < 10; i++) {
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
 * Optimizing bubble sort with flag
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
 * String v. Array
 * Unmutable v. Mutable
 */

var string = '0123456789';
var array = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9'];

console.log(`string: ${string}`, `array: ${array}`);

string[0] = 'A';
array[0] = 'A';

console.log(`string: ${string}`, `array: ${array}`);
```

# Multidimensional Array
```javascript
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

# Modular Function
```javascript
```

# Git Branch, Git Merge and GitHub Pull Request
[Google Slides - Branch, Merge and Pull Request](https://docs.google.com/presentation/d/1-5iMezGG09yLE_tdXxhgzLolvSIR_o0wAWFcwjqs3gk/edit?usp=drivesdk)