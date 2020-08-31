[**Back to Home**](./../README.md)

# Flash Quizes

## Terminal

````
**Flash Quiz!**

```bash
ls ../..
```
Apa yang akan dihasilkan dari command di atas?

:one: Memindahkan working directory ke dua tingkat di atas
:two: Membuat folder baru
:three: Menampilkan isi dari folder yang berada pada dua tingkat di atas working directory
:four: Menghapus semua isi dari folder **System32** :scream: 
:five: Memulai installer Ubuntu
````

````
**Flash Quiz!**

Command terminal apakah yang digunakan untuk menghapus sebuah file?

:one: `delete <nama_file>`
:two: `remove <nama_file>`
:three: `rm <nama_file>`
:four: `destroy <nama_file>`
````

## Variable Declarations

```
**Flash Quiz!**

Pilihan manakah yang merupakan syntax valid JavaScript?

:one: `var naruto == 10`;
:two: `console.log(I am a beautiful butterfly)`;
:three: `var a = 3`;
:four: `var 1thing = 100`;
:five: `console.log['Interesting']`;
```

## Conditionals

````
**Flash Quiz!**

```javascript
var a = 7;
if (a < 10) {
  a = a + 2;
} if (a < 10) {
  a = a + 2;
}

console.log(a);
```
Apa yang akan ditampilkan pada terminal saat kode JavaScript di atas dieksekusi?

:one: 7
:two: 8
:three: 9
:four: 10
:five: 11
````

## Loopings

```
**Flash Quiz!**

Kalian diperintahkan untuk mencari sebuah jarum di tumpukan jerami. Apa yang akan kalian lakukan?

:one: `for`
:two: `loop`
:three: `while`
:four: Yes
:five: No
```

````
**Flash Quiz!**

```javascript
let a = 10;
let sum = 0;
for (let i = 1; i <= a; i++) {
  sum += i;
}
console.log(sum);
```
Apa yang dilakukan oleh kode di atas?

:one: Menjumlahkan angka 0 sampai 10
:two: Menjumlahkan angka 1 sampai 10
:three: Menjumlahkan angka 0 sampai 9
:four: Menjumlahkan angka 1 sampai 9
````

## Arrays and Strings

```
**Flash Quiz!**

Dari pernyataan-pernyataan di bawah, pilih satu pernyataan yang benar mengenai **array** dan **string**!

:one: Indexing tidak dapat dilakukan pada string, namun dapat dilakukan pada array.
:two: Nilai elemen pada suatu string tidak dapat diganti, sedangkan nilai elemen pada suatu array bisa diganti.
:three: String memiliki properti `length`, sedangkan array tidak memiliki properti `length`.
:four: String memiliki built-in function `indexOf()`, sedangkan array tidak.
```

````
**Flash Quiz!**

```javascript
let a = ['Acong', 'Djoko', "Sitorus"];
for (let i = 0; i < a.length; i ++) {
  let out = '';
  for (let j = 0; j < a[0].length; j++) {
    out += a[i][j];
  }
  console.log(out);
}
```
Apa yang ditampilkan pada terminal apabila kode di atas di jalankan?

:one: ```
Acong Djoko Sitorus
```
:two: ```
Acong
Djoko
Sitor
```
:three: ```
Acong
Djoko
Sitorus
```
:four: ```
AcongDjokoSitor
```
````

````
**Flash Quiz!**

```javascript
var arr1 = [1, 2, 3];
var arr2 = arr1;
arr2[0] = 99;
console.log(arr1);
```
Apa yang akan ditampilkan pada terminal apabila kode program di atas dieksekusi?
:one: `[ 1, 2, 3 ]`
:two: `[ '1', '2', '3' ]`
:three: `[ 99, 2, 3 ]`
:four: `[ '99', '2', '3' ]`
````

## Functions

````
**Flash Quiz!**

```javascript
function matematik(num1, num2) {
  let hasil = (num1 + num2) * 0;
  return hasil;
}

matematik(1, 5);
```
Apa yang ditampilkan pada terminal apabila kode di atas di jalankan?

:one: 
:two: 6
:three: 0
:four: 70
````

````
**Flash Quiz!**

```javascript
function matematik(num1, num2) {
  let hasil = (num1 + num2) * 0;
  console.log(hasil);
}

console.log(matematik(1, 5));
```
Apa yang ditampilkan pada terminal apabila kode di atas di jalankan?

:one: ```
0
```
:two: ```
undefined
```
:three: ```
undefined
0
```
:four: ```
0
undefined
```
:five: Yes
````

````
**Flash Quiz!**

```javascript
function matematik(num1, num2) {
  console.log(num1);
  console.log(num2);
}

matematik([1, 2]);
```
Apa yang ditampilkan pada terminal apabila kode di atas di jalankan?

:one: ```
99
```
:two: ```
1, 2
```
:three: ```
[ 1, 2 ]
undefined
```
:four: ```
[ 1, 2 ]
```
````

## Modular Functions

````
**Flash Quiz!**

```javascript
function multiplication(a, b) {
  return a * b;
}

function addition(a, b) {
  return a + b;
}

console.log(multiplication(addition(5, 2), multiplication(3, 5)));
```
Apa yang ditampilkan pada terminal apabila kode di atas dieksekusi?

:one: 99
:two: 150
:three: 25
:four: 105
````

## HTML

```
**Flash Quiz!**

Manakah dari tag berikut ini yang digunakan untuk membuat text memiliki format underline?

:one: `<li></li>`
:two: `<u></u>`
:three: `<b></b>`
:four: `<ul></ul>`
```

```
**Flash Quiz!**

Attribute HTML apa yang digunakan untuk mendefinisikan inline styles?

:one: `font`
:two: `style`
:three: `class`
:four: `styles`
```

## CSS

````
**Flash Quiz!**

```html
  ...
  <style>
    #pidgeonid {
      color: blue;
    }
    .pidgeondiv {
      color: green;
    }
    div {
      color: red;
    }
  </style>
  ...

  ...
  <div class="pidgeondiv" id="pidgeonid">
    I am a beautiful Pidgeon
  </div>
  ...


Apa hasil dari kode HTML di atas?
:one: I am a beautiful Pidgeon [warna biru]
:two: I am a beautiful Pidgeon [warna hijau]
:three: I am a beautiful Pidgeon [warna merah]
:four: I am not a Pidgeon bro [warna rainbow :rainbow: ]

Note: Jangan dicoba pake browser ya :sweat_smile:
````

```
**Flash Quiz!**

Siapakah penggagas CSS pertama kali?

:one: Peter Freuchen
:two: Linus Torvalds
:three: Virat Kohli
:four: Håkon Wium Lie
:five: Conor McGregor
```

[**Back to Home**](./../README.md)
