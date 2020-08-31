[**Back to Home**](./../README.md)

# Looping Review

## Jenis Looping

### for

```javascript
/**
 * Pseudocode:
 *
 * FOR i FROM 0 TO 10 INCREMENT BY 1
 *   ...
 * END FOR
 */

for (var i = 0; i < 10; i++) {
  // do something here
}
```

### while

```javascript
/**
 * Pseudocode:
 *
 * STORE i AS NUMBER WITH VALUE 0
 * WHILE i < 5
 *   ...
 *   SET i TO i + 1
 * END WHILE
 */

var i = 0;
while (i < 5) {
  // do something here
  i++;
}
```

### do...while

```javascript
/**
 * Pseudocode:
 *
 * STORE i AS NUMBER WITH VALUE 0
 * DO
 *   ...
 *   SET i TO i + 1
 * WHILE i < 5
 */

var i = 0;
do {
  // do something here
  i++;
} while (i < 5);
```

## When to use for, while and do...while?

| Syntax       | Bahasa                              |
| ------------ | ----------------------------------- |
| `for`        | Lakukan sesuatu sebanyak x kali     |
| `while`      | Selama kondisi true lakukan sesuatu |
| `do...while` | Lakukan sesuatu selama kondisi true |

## Practices

```javascript
/**
 * Buatlah sebuah program yang akan menerima input kalimat.
 * Program yang dibuat harus menampilkan masing-masing kata dari kalimat tersebut ke bawah.
 * Apabila input adalah kosong, maka tampilkan "Invalid input".
 * 
 * Contoh:
 *   - Input  : 'Bagong pergi mencari jus jeruk'
 *   - Output : 'Bagong'
 *              'pergi'
 *              'mencari'
 *              'jus'
 *              'jeruk'
 */

var input = 'Bagong pergi mencari jus jeruk';

if (input) {
  // code here
  var toDisplay = '';
  for (var i = 0; i < input.length; i++) {
    if (input[i] === ' ') {
      console.log(toDisplay);
      toDisplay = '';
    } else {
      // toDisplay = toDisplay + input[i];
      toDisplay += input[i];
    }

    if (i === input.length - 1) {
      console.log(toDisplay);
    }
  }
} else {
  console.log('Input invalid');
}
```

```javascript
/**
 * Buatlah sebuah program yang akan mengurutkan huruf dari sebuah input string.
 * 
 * Contoh 1:
 *   - Input  : javascript
 *   - Output : aacijprstv
 * 
 * Contoh 2:
 *   - Input  : fedcba
 *   - Output : abcdef
 */

var input = 'javascript';
var kamus = 'abcdefghijklmnopqrstuvwxyz';
var output = '';

for (var i = 0; i < kamus.length; i++) {
  for (var j = 0; j < input.length; j++) {
    if (kamus[i] === input[j]) {
      output += kamus[i];
    }
  }
}

console.log(output);
```

```javascript
/**
 * Buatlah sebuah program yang akan mensimulasikan sebuah gacha pada permainan.
 * Ketentuan dari gacha tersebut adalah:
 *   - Karakter SSS memiliki 1% chance
 *   - Karakter SS memiliki 5% chance
 *   - Karakter S memiliki 10% chance
 *   - Karakter A memiliki 20% chance
 *   - Karakter B memiliki 64% chance
 * 
 * Output dari program tersebut adalah jumlah roll yang harus dilakukan sampai mendapatkan
 * karakter SSS. Format output yang diharapkan:
 * 'Jumlah roll yang dilakukan <jumlah_roll>'
 */

var roll = 0;
var karakter = 0;
var count = 0;

do {
  karakter = Math.floor(Math.random() * 100) + 1;
  count++;

} while (karakter !== 1);

console.log(`Jumlah roll yang dilakukan ${count}`);
```

```javascript
/**
 * Buatlah sebuah program yang akan mencari sebuah string di dalam string.
 * String input akan terdapat pada variable input.
 * String yang dicari akan terdapat pada variable search.
 *
 * Output yang diharapkan dari program adalah:
 *   - true  : jika search terdapat dalam input
 *   - false : jika search tidak terdapat dalam input
 */

var input = "Fisika SMA Terpadu Kelas XI";
var search = "SMA";
```

[**Back to Home**](./../README.md)
