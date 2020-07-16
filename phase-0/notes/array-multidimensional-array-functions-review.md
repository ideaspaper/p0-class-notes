[**Back to Home**](./../README.md)

# Array, Multidimensional Array and Functions Review

## Latihan 1

```javascript
/**
 * Sebuah bioskop hendak membuat highlight untuk film-film dengan penilaian terbaik.
 * Film-film yang akan masuk ke dalam highlight merupakan film dengan total score 300 ke atas.
 * Adapun perhitungan score tersebut adalah dari rating * jumlah review.
 * Buatlah sebuah program untuk menentukan film-film yang akan masuk ke dalam highlight tersebut.
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

function hightlight(input, score) {
  // Code here
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
  // Code here
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

[Answers](./array-multidimensional-array-functions-review-answered.md)

[**Back to Home**](./../README.md)
