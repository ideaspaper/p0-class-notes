# Table of Contents
### [HTML](#html)
### [CSS](#css)
### [Algorithm and Pseudocode](#algorithm-and-pseudocode)
### [Conditional and Primitive Data Types](#conditional-and-primitive-data-types)
### [Multidimensional Array](#multidimensional-array)

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
```JavaScript
```

# Pseudocode and Looping
```JavaScript
```

# Nested Conditional
```JavaScript
```

# Function
```JavaScript
```

# Array
```JavaScript
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

```JavaScript
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

```JavaScript
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

```JavaScript
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

```JavaScript
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
```JavaScript
```
    

# Array of Object
```JavaScript
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

```JavaScript
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

```JavaScript
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

```JavaScript
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

```JavaScript
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

```JavaScript
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
```JavaScript
```

# Git Branch, Git Merge and GitHub Pull Request
[Google Slides - Branch, Merge and Pull Request](https://docs.google.com/presentation/d/1-5iMezGG09yLE_tdXxhgzLolvSIR_o0wAWFcwjqs3gk/edit?usp=drivesdk)