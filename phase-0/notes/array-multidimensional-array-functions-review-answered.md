[**Back to Home**](./../README.md)

# Array, Multidimensional Array and Functions Review

## Latihan 1

```javascript
/**
 * Sebuah bioskop hendak membuat highlight untuk film-film dengan penilaian terbaik.
 * Secara default, film-film yang akan masuk ke dalam highlight merupakan film dengan total score 300 ke atas.
 * Adapun perhitungan score tersebut adalah dari rating * jumlah review.
 * Buatlah sebuah program untuk menentukan film-film yang akan masuk ke dalam highlight tersebut.
 *
 * Note: apabila parameter score tidak diisi, maka diasumsikan nilai yang digunakan adalah 300.
 */

// [ judul film, rating, jumlah review ]
let movies = [
  ['Parasite', '★★★★★', 93],
  ['Moonlight', '★★☆☆☆', 60],
  ['Captain Marvel', '★★★★☆', 64],
  ['The Irishman', '★★★★☆', 86],
  ['Inception', '★★★☆☆', 72],
  ['Toy Story 3', '★★★★☆', 98],
  ['Citizen Kane', '★★★☆☆', 66]
];

function hightlight(input, score = 300) {
  let ret = [];

  for(let i = 0; i < input.length; i++) {
    let j = 0;
    while (input[i][1][j] === '★') {
      j++;
    }
    input[i].push(j * input[i][2]);
    if (input[i][3] >= score) {
      ret.push(input[i]);
    }
  }

  return ret;
}

console.log(hightlight(movies));
/**
 * [
 *   [ 'Parasite', '★★★★★', 93, 465 ],
 *   [ 'The Irishman', '★★★★☆', 86, 344 ],
 *   [ 'Toy Story 3', '★★★★☆', 98, 392 ]
 * ]
 */

console.log(hightlight(movies, 400));
/**
 * [ [ 'Parasite', '★★★★★', 93, 465 ] ]
 */
```

## Latihan 2

```javascript
/**
 * Terdapat sebuah playlist lagu berupa array multidimensi.
 * Buatlah sebuah program yang akan menampilkan lagu-lagu apa saja yang akan dimainkan berdasarkan alokasi waktu yang diberikan.
 * Ketentuan memainkan lagu adalah sebagai berikut:
 *   - Apabila waktu tidak cukup untuk memainkan 1 lagu secara penuh, maka lagu tersebut batal dimainkan.
 *   - Apabila lagu paling akhir sudah dicapai, maka proses akan kembali ke lagu pertama.
 *   - Apabila parameter time tidak diisi, maka semua lagu akan dimainkan berurutan sekali saja.
 */

// [ penyanyi, judul lagu, durasi ]
let playlist = [
  ['Didi Kempot', 'Banyu Langit', 4],
  ['Nike Ardilla', 'Sandiwara Cinta', 4],
  ['Hetty Koes Endang', 'Cinta Putih', 3],
  ['Titiek Puspa', 'Kupu-Kupu Malam', 3],
  ['Ahmad Albar', "Don't Spoil My Day", 5],
  ['Doel Sumbang', 'Awewe Sapi Daging', 2],
  ['Ebiet G. Ade', 'Berita Kepada Kawan', 6]
];

function play(input, time) {
  if (!time) {
    return input;
  }

  let ret = [];

  let index = 0;
  while (time >= 0) {
    time -= input[index][2];
    if (time >= 0) {
      ret.push(input[index]);
    }
    index++;
    if (index === input.length) {
      index = 0;
    }
  }

  return ret;
}

console.log(play(playlist));
/**
 * [
 *   [ 'Didi Kempot', 'Banyu Langit', 4 ],
 *   [ 'Nike Ardilla', 'Sandiwara Cinta', 4 ],
 *   [ 'Hetty Koes Endang', 'Cinta Putih', 3 ],
 *   [ 'Titiek Puspa', 'Kupu-Kupu Malam', 3 ],
 *   [ 'Ahmad Albar', "Don't Spoil My Day", 5 ],
 *   [ 'Doel Sumbang', 'Awewe Sapi Daging', 2 ],
 *   [ 'Ebiet G. Ade', 'Berita Kepada Kawan', 6 ]
 * ]
 */

console.log(play(playlist, 9));
/**
 * [
 *   ['Didi Kempot', 'Banyu Langit', 4],
 *   ['Nike Ardilla', 'Sandiwara Cinta', 4]
 * ]
 */

console.log(play(playlist, 32));
/**
 * [
 *   [ 'Didi Kempot', 'Banyu Langit', 4 ],
 *   [ 'Nike Ardilla', 'Sandiwara Cinta', 4 ],
 *   [ 'Hetty Koes Endang', 'Cinta Putih', 3 ],
 *   [ 'Titiek Puspa', 'Kupu-Kupu Malam', 3 ],
 *   [ 'Ahmad Albar', "Don't Spoil My Day", 5 ],
 *   [ 'Doel Sumbang', 'Awewe Sapi Daging', 2 ],
 *   [ 'Ebiet G. Ade', 'Berita Kepada Kawan', 6 ],
 *   [ 'Didi Kempot', 'Banyu Langit', 4 ]
 * ]
 */
```

## Latihan 3
```javascript
/**
 * Terdapat sebuah list buku berupa array multidimensi.
 * Buatlah sebuah program yang akan melakukan pencarian buku-buku yang sesuai dengan sebuah search keyword.
 * Keyword tersebut akan dibandingkan dengan judul buku, nama pengarang, serta penerbit.
 * Hasil yang diharapkan berupa array multidimensi berisi buku-buku yang ditemukan.
 */

// [ judul buku, pengarang, penerbit ]
let books = [
  ['Fisika Terpadu - SMA', 'Bob Foster', 'Erlangga'],
  ['Biologi Dasar - SMA', 'Irnaningtyas', 'Erlangga'],
  ['Harry Potter', 'J. K. Rowling', 'Gramedia'],
  ['Pemrograman Web dengan Node.js dan Javascript', 'Budi Raharjo', 'Informatika'],
  ['Ruby untuk Aplikasi Desktop dan Web', 'Budi Raharjo', 'Informatika']
]

function searchAll(input, search) {
  // Code here
  let ret = [];

  for (let i = 0; i < input.length; i++) {
    for (let j = 0; j < input[i].length; j++) {
      let found = false;
      for (let k = 0; k < input[i][j].length; k++) {
        let count = 0;
        if (input[i][j][k] === search[0]) {
          for (let l = 0; l < search.length; l++) {
            if (input[i][j][k + l] === search[l]) {
              count++;
            }
          }
          if (count === search.length) {
            found = true;
            break;
          }
        }
      }
      if (found) {
        ret.push(input[i])
      }
    }
  }

  return ret;
}

console.log(searchAll(books, ''));
/**
 * []
 */

console.log(searchAll(books, 'Erlangga'));
/**
 * [
 *   [ 'Fisika Terpadu - SMA', 'Bob Foster', 'Erlangga' ],
 *   [ 'Biologi Dasar - SMA', 'Irnaningtyas', 'Erlangga' ]
 * ]
 */

console.log(searchAll(books, 'dan'));
/**
 * [
 *   [
 *     'Pemrograman Web dengan Node.js dan Javascript',
 *     'Budi Raharjo',
 *     'Informatika'
 *   ],
 *   [
 *     'Ruby untuk Aplikasi Desktop dan Web',
 *     'Budi Raharjo',
 *     'Informatika'
 *   ]
 * ]
 */
```

```javascript
/**
 * Search substring in string example
 */

let sentence = 'Budi Raharjo';
let search = 'udi';

let found = false;
for (let k = 0; k < sentence.length; k++) {
  let count = 0;
  if (sentence[k] === search[0]) {
    for (let l = 0; l < search.length; l++) {
      if (sentence[k + l] === search[l]) {
        count++;
      }
    }
    if (count === search.length) {
      found = true;
      break;
    }
  }
}

console.log(found);
```

[**Back to Home**](./../README.md)
