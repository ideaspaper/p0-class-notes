[**Back to Home**](./../README.md)

# Object Literal

[Object Literal](./../assets/object-literal.pdf)

## Object Literal Behaviour

- Menambahkan number atau string sebagai key.

  ```javascript
  let a = {};
  a[1] = "this is 1";
  a[0] = "this is 0";
  console.log(a);
  
  let b = {};
  b["c"] = "this is c";
  b["a"] = "this is a";
  console.log(b);
  
  let c = {};
  c[20] = "this is 20";
  c[10020] = "this is 10020";
  c["c"] = "this is c";
  c["a"] = "this is a";
  console.log(c);
  ```

- Menambahkan key yang sudah ada sebelumnya.

  ```javascript
  let a = {
    key1: 'String',
    key2: 10,
    key3: true
  };
  console.log(a);
  a.key1 = 99;
  console.log(a);
  ```

## Practices

```javascript
/**
 * Buat key baru yaitu sellPrice pada product, dengan value:
 *   sellPrice = (price + (price * profit / 100))
 */

let profit = 10;

let product = {
  name: "Baygon",
  form: "Aerosol",
  bugType: "Roaces",
  price: 15000,
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
  name: "Sensebounce+ SUMMER.RDY Shoes",
  manufacturer: "Adidas",
  gender: "Men",
  sport: "Running",
  weightGram: 366,
  colors: ["Black", "White"],
  warehouseStock: {
    warehouse1: 0,
    warehouse2: 10,
    warehouse3: 2,
  },
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

let a = { key1: "A", key2: 10, key3: true };
let b = { key1: "A", key2: 10, key3: true };
let c = { key1: 11, key2: "B", key3: true };

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
  ["Acong", "Mual"],
  ["Djoko", "Pusing"],
  ["Sitorus", "Batuk"],
  ["Rama", "Pusing"],
  ["Shinta", "Batuk"],
  ["Cthulhu", "Mual"],
  ["Nyarlothep", "Mual"],
];

function groupByIllness() {
  // Do something here
}

console.log(groupByIllness(patients));
// {
//   Mual: [ 'Acong', 'Cthulhu', 'Nyarlothep' ],
//   Pusing: [ 'Djoko', 'Rama' ],
//   Batuk: [ 'Sitorus', 'Shinta' ]
// }
```

[Answers](./object-literal-answered.md)

[**Back to Home**](./../README.md)
