[**Back to Home**](./../README.md)

# Object Literal Review

## Soal 1

```javascript
/**
 * Buatlah sebuah function untuk menghilangkan elemen-elemen duplikat yang terdapat dalam array.
 * Elemen pada array bisa bertipe number ataupun string.
 * Kerjakan soal berikut menggunakan object.
 */
function arrSet(input) {
  let obj = {};
  for (let i = 0; i < input.length; i++) {
    if (!(input[i] in obj)) {
      obj[input[i]] = input[i];
    }
  }
  return Object.values(obj);
}

console.log(arrSet([1, 1, 1, 3, 3, 3, 5, 5, 5, 5]));        // [ 1, 3, 5 ]
console.log(arrSet([1, 5, 1, 2, 2, 3, 3, 5, 5]));           // [ 1, 2, 3, 5 ]
console.log(arrSet([1, 5, 1, 2, 2, 3, 3, 5, 5, 'A', 'A'])); // [ 1, 2, 3, 5, 'A' ]
```

## Soal 2

```javascript
/**
 * Asumsikan perhitungan umur menggunakan referensi tahun 2020.
 */

function groupByAge(arr) {
  let ret = {};
  for (let i = 0; i < arr.length; i++) {
    if (!((2020 - arr[i]) in ret)) {
      ret[2020 - arr[i]] = 0;
    }
    ret[2020 - arr[i]]++;
  }
  return ret;
}

console.log(groupByAge([2003, 1991, 1821, 2003, 1821, 1995, 1995]))
// {
//   '17': 2,
//   '25': 2,
//   '29': 1,
//   '199': 2
// }
```

## Soal 3
```js
/**
 * Buat sebuah function yang akan menghasilkan array of string yang berisi,
 * hobi-hobi yang sama antara dua orang. Seseorang direpresentasikan dalam bentuk object
 * seperti di bawah:
 * 
 * {
 *   name: 'semmi',
 *   hobbies: ['Sleeping', 'Dancing', 'Coding']
 * }
 */

function sameHobbies(obj1, obj2) {
  let temp1
  let temp2;
  if (obj2.hobbies.length > obj1.hobbies.length) {
    temp1 = obj2;
    temp2 = obj1;
  } else {
    temp1 = obj1;
    temp2 = obj2;
  }

  let ret = [];
  for (let i = 0; i < temp1.hobbies.length; i++) {
    for (let j = 0; j < temp2.hobbies.length; j++) {
      if (temp1.hobbies[i] === temp2.hobbies[j]) {
        ret.push(temp1.hobbies[i]);
        break;
      }
    }
  }

  return ret;
}

let semmi = {
  name: 'semmi',
  hobbies: ['Sleeping', 'Dancing', 'Coding']
}

let bimo = {
  name: 'bimo',
  hobbies: ['Sleeping', 'Cooking', 'Coding', 'Cleaning']
}

console.log(sameHobbies(semmi, bimo)) // ['Sleeping', 'Coding']
```

## Soal 4

```javascript
/**
 * Terdapat sebuah perusahaan furniture yang hendak membuat software untuk menghitung production cost
 * dari permintaan-permintaan yang ada. Kriteria penentuan cost produksi sebuah produk dibagi menjadi 3
 * yaitu jenis produk, ukuran, serta material.
 * 
 * Buatlah sebuah function untuk permasalahan tersebut. Function akan memiliki 4 buah parameter yaitu:
 *   - product yang akan menerima argumen berupa object seperti di bawah
 *     {
 *       lemari: 32000,
 *       meja: 22000,
 *       kursi: 14000
 *     }
 *   - size yang akan menerima argumen berupa object seperti di bawah
 *     {
 *       besar: 31000,
 *       sedang: 21500,
 *       kecil: 18000
 *     }
 *   - material yang akan menerima argumen berupa object seperti di bawah
 *     {
 *       jati: 40000,
 *       stainless: 35000,
 *       kayu: 27500,
 *       plastik: 13000
 *     }
 *   - demands yang akan menerima argumen berupa object seperti di bawah
 *     {
 *       demand1: [
 *         ['meja', 'sedang', 'kayu'],
 *         ['lemari', 'besar', 'kayu'],
 *         ['meja', 'kecil', 'plastik']
 *       ],
 *       demand2: [
 *         ['kursi', 'besar', 'jati'],
 *         ['meja', 'besar', 'stainless']
 *       ],
 *       demand3: [
 *         ['meja', 'kecil', 'plastik'],
 *         ['meja', 'sedang', 'jati'],
 *         ['kursi', 'kecil', 'jati']
 *       ]
 *     }
 * 
 * Hasil yang diharapkan dari fungsi tersebut adalah sebuah object seperti di bawah
 * {
 *   demand1: 214500,
 *   demand2: 173000,
 *   demand3: 208500
 * }
 * 
 * Nilai 173000 pada demand2 didapatkan dari:
 *   ['kursi', 'besar', 'jati']     --> 14000 + 31000 + 40000 = 85000 ┬─[ + ]── 173000
 *   ['meja', 'besar', 'stainless'] --> 22000 + 31000 + 35000 = 88000 ┘
 */

function getProductionCost(product, size, material, demands) {
  for (const key in demands) {
    let temp = 0;
    for (let i = 0; i < demands[key].length; i++) {
      temp += product[demands[key][i][0]] + size[demands[key][i][1]] + material[demands[key][i][2]];
    }
    demands[key] = temp;
  }
  return demands;
}

console.log(getProductionCost({
  lemari: 32000,
  meja: 22000,
  kursi: 14000
}, {
  besar: 31000,
  sedang: 21500,
  kecil: 18000
}, {
  jati: 40000,
  stainless: 35000,
  kayu: 27500,
  plastik: 13000
}, {
  demand1: [
    ['meja', 'sedang', 'kayu'],
    ['lemari', 'besar', 'kayu'],
    ['meja', 'kecil', 'plastik']
  ],
  demand2: [
    ['kursi', 'besar', 'jati'],
    ['meja', 'besar', 'stainless']
  ],
  demand3: [
    ['meja', 'kecil', 'plastik'],
    ['meja', 'sedang', 'jati'],
    ['kursi', 'kecil', 'jati']
  ]
}));
// { demand1: 214500, demand2: 173000, demand3: 208500 }
```

[**Back to Home**](./../README.md)
