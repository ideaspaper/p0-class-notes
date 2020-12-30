[**Back to Home**](./../README.md)

# Flash Quizes

## Terminal

## Terminal

````
/poll "**Flash Quiz!**

```bash
ls ../..
```
Apa yang akan dihasilkan dari command di atas?"

"Memindahkan working directory ke dua tingkat di atas"
"Membuat folder baru"
"Menampilkan isi dari folder yang berada pada dua tingkat di atas working directory"
"Menghapus semua isi dari folder **System32** :scream:"
"Memulai installer Ubuntu"
````

````
/poll "**Flash Quiz!**

Command terminal apakah yang digunakan untuk menghapus sebuah file?"

"`delete <nama_file>`"
"`remove <nama_file>`"
"`rm <nama_file>`"
"`destroy <nama_file>`"
````

## Variables

```
/poll "**Flash Quiz!**

Pilihan manakah yang merupakan syntax valid JavaScript?"

"`var naruto == 10`;"
"`console.log(I am a beautiful butterfly)`;"
"`var a = 3`;"
"`var 1thing = 100`;"
"`console.log['Interesting']`;"
```

````
/poll "**Flash Quiz!**

```javascript
var a = 5;
var b = 3;

// Solusi
```
Diberikan dua buah variable yaitu `a` dan `b`. Solusi manakah yang paling tepat untuk menukar nilai `a` menjadi nilai `b`, begitu pula sebaliknya?
Note: nilai `a` dan `b` bisa berapa saja."

"
```javascript
a = 3;
b = 5;
```
"
"
```javascript
var a = 3;
var b = 5;
```
"
"
```javascript
a = b;
b = a;
```
"
"
```javascript
var c = a;
a = b;
b = c;
```
"
"
```javascript
var c = b;
a = b;
b = a;
```
"
````

## Conditionals

````
/poll "**Flash Quiz!**

```javascript
var a = 7;
if (a < 10) {
  a = a + 2;
} if (a < 10) {
  a = a + 2;
}

console.log(a);
```
Apa yang akan ditampilkan pada terminal saat kode JavaScript di atas dieksekusi?"

"7"
"8"
"9"
"10"
"11"
````

## Loopings

```
/poll "**Flash Quiz!**

Kalian diperintahkan untuk mencari sebuah jarum di tumpukan jerami. Apa yang akan kalian lakukan?"

"`for`"
"`loop`"
"`while`"
"Yes"
"No"
```

````
/poll "**Flash Quiz!**

```javascript
let a = 10;
let sum = 0;
for (let i = 1; i <= a; i++) {
  sum += i;
}
console.log(sum);
```
Apa yang dilakukan oleh kode di atas?"

"Menjumlahkan angka 0 sampai 10"
"Menjumlahkan angka 1 sampai 10"
"Menjumlahkan angka 0 sampai 9"
"Menjumlahkan angka 1 sampai 9"
````

## Arrays and Strings

```
/poll "**Flash Quiz!**

Dari pernyataan-pernyataan di bawah, pilih satu pernyataan yang benar mengenai **array** dan **string**!"

"Indexing tidak dapat dilakukan pada string, namun dapat dilakukan pada array."
"Nilai elemen pada suatu string tidak dapat diganti, sedangkan nilai elemen pada suatu array bisa diganti."
"String memiliki properti `length`, sedangkan array tidak memiliki properti `length`."
"String memiliki built-in function `indexOf()`, sedangkan array tidak."
```

````
/poll "**Flash Quiz!**

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
Apa yang ditampilkan pada terminal apabila kode di atas di jalankan?"

"
```
Acong Djoko Sitorus
```
"
"
```
Acong
Djoko
Sitor
```
"
"
```
Acong
Djoko
Sitorus
```
"
"
```
AcongDjokoSitor
```
"
````

````
/poll "**Flash Quiz!**

```javascript
var arr1 = [1, 2, 3];
var arr2 = arr1;
arr2[0] = 99;
console.log(arr1);
```
Apa yang akan ditampilkan pada terminal apabila kode program di atas dieksekusi?"
"`[ 1, 2, 3 ]`"
"`[ '1', '2', '3' ]`"
"`[ 99, 2, 3 ]`"
"`[ '99', '2', '3' ]`"
````

## Functions

````
/poll "**Flash Quiz!**

```javascript
function matematik(num1, num2) {
  let hasil = (num1 + num2) * 0;
  return hasil;
}

matematik(1, 5);
```
Apa yang ditampilkan pada terminal apabila kode di atas di jalankan?"

""
"6"
"0"
"70"
````

````
/poll "**Flash Quiz!**

```javascript
function matematik(num1, num2) {
  let hasil = (num1 + num2) * 0;
  console.log(hasil);
}

console.log(matematik(1, 5));
```
Apa yang ditampilkan pada terminal apabila kode di atas di jalankan?"

"
```
0
```
"
"
```
undefined
```
"
"
```
undefined
0
```
"
"
```
0
undefined
```
"
"Yes"
````

````
/poll "**Flash Quiz!**

```javascript
function matematik(num1, num2) {
  console.log(num1);
  console.log(num2);
}

matematik([1, 2]);
```
Apa yang ditampilkan pada terminal apabila kode di atas di jalankan?"

"
```
99
```
"
"
```
1, 2
```
"
"
```
[ 1, 2 ]
undefined
```
"
"
```
[ 1, 2 ]
```
"
````

## Modular Functions

````
/poll "**Flash Quiz!**

```javascript
function multiplication(a, b) {
  return a * b;
}

function addition(a, b) {
  return a + b;
}

console.log(multiplication(addition(5, 2), multiplication(3, 5)));
```
Apa yang ditampilkan pada terminal apabila kode di atas dieksekusi?"

"99"
"150"
"25"
"105"
````

## HTML

```
/poll "**Flash Quiz!**

Manakah dari tag berikut ini yang digunakan untuk membuat text memiliki format underline?"

"`<li></li>`"
"`<u></u>`"
"`<b></b>`"
"`<ul></ul>`"
```

```
/poll "**Flash Quiz!**

Attribute HTML apa yang digunakan untuk mendefinisikan inline styles?"

"`font`"
"`style`"
"`class`"
"`styles`"
```

## CSS

````
/poll "**Flash Quiz!**

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


Apa hasil dari kode HTML di atas?"
"I am a beautiful Pidgeon [warna biru]"
"I am a beautiful Pidgeon [warna hijau]"
"I am a beautiful Pidgeon [warna merah]"
"I am not a Pidgeon bro [warna rainbow :rainbow: ]"
````

```
/poll "**Flash Quiz!**

Siapakah penggagas CSS pertama kali?"

"Peter Freuchen"
"Linus Torvalds"
"Virat Kohli"
"Håkon Wium Lie"
"Conor McGregor"
```

[**Back to Home**](./../README.md)
