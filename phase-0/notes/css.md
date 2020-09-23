[**Back to Home**](./../README.md)

# CSS

CSS merupakan bahasa yang digunakan untuk mendeskripsikan bagaimana sebuah dokumen HTML harus dipresentasikan.

Contoh syntax CSS adalah sebagai berikut:

```css
h1 {
  color: blue;
  font-size: 12px;
}
```

- `h1` merupakan selector.
- `color` dan `font-size` merupakan properti.
- `blue` dan `12px` merupakan value.

Pada syntax di atas, kita hendak membuat semua elemen HTML yang memiliki tag `h1` agar memiliki warna text biru serta ukuran huruf sebesar 12 pixel.

## Selector

Selector digunakan untuk menunjuk elemen HTML mana yang hendak kita ubah styling-nya menggunakan CSS. Terdapat 4 buah selector dasar pada CSS sebagai berikut:

- **#id**

  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Document</title>
      <style>
        #special {
          color: orange;
        }
      </style>
    </head>
    <body>
      <h1 id="special">This is h1 with id special</h1>
      <h1>This is h1 without id</h1>
    </body>
  </html>
  ```

- **tag**

  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Document</title>
      <style>
        h1 {
          color: blue;
        }
      </style>
    </head>
    <body>
      <h1>This is 1st h1</h1>
      <h2>This is 1st h2</h2>
      <h1>This is 2nd h1</h1>
      <h2>This is 2nd h2</h2>
    </body>
  </html>
  ```

- **.class**

  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Document</title>
      <style>
        a {
          text-decoration: none;
          font-size: x-large;
        }
        .active-link {
          color: green;
        }
        .inactive-link {
          color: red;
        }
      </style>
    </head>
    <body>
      <a href="#" class="active-link">This is link 1 (active)</a>
      <a href="#" class="active-link">This is link 2 (active)</a>
      <a href="#" class="inactive-link">This is link 3 (disabled)</a>
      <a href="#" class="inactive-link">This is link 4 (disabled)</a>
      <a href="#" class="active-link">This is link 5 (active)</a>
    </body>
  </html>
  ```

- **\***

  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Document</title>
      <style>
        * {
          color: white;
          background-color: black;
        }
      </style>
    </head>
    <body>
      <a href="#" class="active-link">This is link 1 (active)</a>
      <a href="#" class="active-link">This is link 2 (active)</a>
      <a href="#" class="inactive-link">This is link 3 (disabled)</a>
      <a href="#" class="inactive-link">This is link 4 (disabled)</a>
      <a href="#" class="active-link">This is link 5 (active)</a>
    </body>
  </html>
  ```

  [CSS selector reference](https://www.w3schools.com/cssref/css_selectors.asp)

## Styling Method

- **Inline**

  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Document</title>
      <link rel="stylesheet" href="styles.css" />
    </head>
    <body>
      <h1 style="color: blue;">This is a heading</h1>
      <p style="color: red;">This is a paragraph.</p>
    </body>
  </html>
  ```

- **Internal**

  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Document</title>
      <style>
        #special {
          color: orange;
        }
      </style>
    </head>
    <body>
      <h1 id="special">This is h1 with id special</h1>
      <h1>This is h1 without id</h1>
    </body>
  </html>
  ```

- **External**

  `styles.css`
  
  ```css
  #special {
    color: orange;
  }
  ```

  `index.html`
  
  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Document</title>
      <link rel="stylesheet" href="styles.css">
    </head>
    <body>
      <h1 id="special">This is h1 with id special</h1>
      <h1>This is h1 without id</h1>
    </body>
  </html>
  ```

### Sequence of Declaration

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      #special {
        color: orange;
      }
      h1 {
        color: green;
      }
      #special {
        color: blue;
      }
    </style>
  </head>
  <body>
    <h1 id="special">This is h1 with id special</h1>
    <h1>This is h1 without id</h1>
  </body>
</html>
```

Warna dari tag `h1` dengan id `special` menjadi biru. Hal tersebut dikarenakan styling terakhir adalah style yang akan digunakan.

Bagaimana apabila seperti di bawah?

`styles.css`

```css
#special {
  color: orange;
}
```

`index.html`

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <h1 id="special" style="color: blue;">This is h1 with id special</h1>
    <h1>This is h1 without id</h1>
    <link rel="stylesheet" href="styles.css">
  </body>
</html>
```

Warna akhir dari tag `h1` dengan id `special` menjadi biru. Hal tersebut karena inline CSS akan selalu mendapatkan prioritas tertinggi (pengecualian untuk [`!important`](https://stackoverflow.com/questions/9245353/what-does-important-mean-in-css)).

## Specificity

Selain dari sequence, styling yang akan digunakan juga ditentukan dari specificity. Semakin spesifik sebuah rule CSS, maka semakin tinggi prioritas rule tersebut untuk digunakan. Secara sederhana:

**`* < tag < .class < #id < !important`**

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      #id-of-h1 {
        color: red;
      }
      .class-of-h1 {
        color: green;
      }
      h1 {
        color: blue;
      }
    </style>
  </head>
  <body>
    <h1>This is h1</h1>
    <h1 class="class-of-h1">This is h1 with class</h1>
    <h1 id="id-of-h1">This is h1 with id</h1>
  </body>
</html>
```

Amati hasilnya. Kemudian coba tambahkan rule berikut sebelum `#id-of-h1`:

```css
* {
  color: yellow !important;
}
```

Hasil dari menambahkan rule tersebut adalah semua rule yang telah dibuat sebelumnya akan diabaikan.

> In CSS, the !important means that “this is important”, ignore all the subsequent rules, and apply !important rule. [source](https://www.geeksforgeeks.org/how-to-apply-important-in-css/)

[Specificity reference](https://specifishity.com/)

[Strategies for Keeping CSS Specificity Low](https://css-tricks.com/strategies-keeping-css-specificity-low/)

## Display Property

Contoh pengaturan display property pada CSS:

```css
.ex1 {
  display: none;
}
.ex2 {
  display: inline;
}
.ex3 {
  display: block;
}
.ex4 {
  display: inline-block;
}
```

[w3schools reference](https://www.w3schools.com/cssref/pr_class_display.asp)

## Box Model

Semua elemen pada dokumen HTML dapat dianggap sebagai sebuah box. Sebuah box memiliki 4 bagian yaitu:

- Margin (transparan)
- Border
- Padding (transparan)
- Content

Contoh pengaturan box model pada CSS:

```css
div {
  width: 300px;
  border: 15px solid green;
  padding: 50px;
  margin: 20px;
}
```

[w3schools reference](https://www.w3schools.com/css/css_boxmodel.asp)

## Font Property

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      p {
        font-family: 'Courier New', Courier, monospace;
        font-size: x-large;
        color: brown;
        text-align: left;
      }
    </style>
  </head>
  <body>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloremque rem
      distinctio libero fuga inventore? Similique, architecto corrupti? Ducimus
      hic doloribus placeat delectus eius reprehenderit consectetur molestias
      nesciunt, a officiis illum!
    </p>
  </body>
</html>
```

`font-family` digunakan untuk memilih font yang akan digunakan pada sebuah element. Apabila pada value dituliskan lebih dari 1 jenis font, maka jenis font yang paling kiri akan digunakan terlebih dahulu. Namun jika font tersebut tidak tersedia, maka jenis font berikutnya yang akan digunakan.

> Start with the font you want, and always end with a generic family, to let the browser pick a similar font in the generic family, if no other fonts are available. [source](https://www.w3schools.com/cssref/pr_font_font-family.asp)

## Units

Unit merupakan size suatu element pada CSS. Unit dapat berupa nilai absolute seperti px, ataupun relative seperti em dan rem.

[CSS units reference](https://www.w3schools.com/cssref/css_units.asp)

## :hover

`:hover` digunakan untuk menerapkan rule styling ketika terjadi event mouse-over pada elemen yang bersangkutan.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      .ex1:hover {
        color: white;
        background-color: black;
        cursor: pointer;
      }
      .ex2:hover {
        color: white;
        background-color: green;
        cursor: not-allowed;
      }
    </style>
  </head>
  <body>
    <h1 class="ex1">This is h1 ex1</h1>
    <h1 class="ex2">This is h1 ex2</h1>
  </body>
</html>
```

## Further Reading

- [Box Shadow](www.cssmatic.com/box-shadow)
- [Display Flex](https://www.w3schools.com/css/css3_flexbox.asp)
- [Selain :hover](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

[**Back to Home**](./../README.md)
