[**Back to Home**](./../README.md)

# Introduction to DOM

DOM adalah kependekan dari (Document Object Model). DOM merupakan antarmuka pemrograman untuk HTML. Dengan antarmuka tersebut, kita dapat mengganti data yang ada pada HTML melalui kode program. DOM dapat diilustrasikan sebagai sebuah tree seperti di bawah.

```
             ╭────────────────╮
             │ HTML           │
             │ [Root Element] │
             ╰────────┬───────╯
      ╭───────────────┴──────────────╮
╭─────┴─────╮                  ╭─────┴─────╮
│ Head      │                  │ Body      │
│ [Element] │                  │ [Element] │
╰─────┬─────╯                  ╰─────┬─────╯
      │                              ├─────────────────────────────────╮
╭─────┴─────╮                  ╭─────┴─────╮   ╭─────────────╮   ╭─────┴─────╮   ╭─────────────╮
│ Title     │                  │ h1        ├───┤ style       │   │ a         ├───┤ href        │
│ [Element] │                  │ [Element] │   │ [Attribute] │   │ [Element] │   │ [attribute] │
╰─────┬─────╯                  ╰─────┬─────╯   ╰─────────────╯   ╰─────┬─────╯   ╰─────────────╯
╭─────┴─────╮                 ╭──────┴──────╮                    ╭─────┴─────╮
│ My Title  │                 │ Hello World │                    │ Link text │
│ [Text]    │                 │ [Text]      │                    │ [Text]    │
╰───────────╯                 ╰─────────────╯                    ╰───────────╯
```


Setiap object yang ada pada DOM merupakan `node`. Pada HTML, object bisa merupakan `element node`, `text node`, atau `attribute node`.

Contoh sebuah HTML dan representasi DOM-nya.

```html
<html>
  <head> </head>
  <body>
    <h1 style="font=weight: bold;">
      Hello World
    </h1>
  </body>
</html>
```

```
             ╭────────────────╮
             │ HTML           │
             │ [Root Element] │
             ╰────────┬───────╯
      ╭───────────────┴──────────────╮
╭─────┴─────╮                  ╭─────┴─────╮
│ Head      │                  │ Body      │
│ [Element] │                  │ [Element] │
╰───────────╯                  ╰─────┬─────╯
                               ╭─────┴─────╮   ╭─────────────╮
                               │ h1        │───│ style       │
                               │ [Element] │   │ [Attribute] │
                               ╰─────┬─────╯   ╰─────────────╯
                              ╭──────┴──────╮
                              │ Hello World │
                              │ [Text]      │
                              ╰─────────────╯
```

## `document.getElementById(id)`

_**Parameters**_

- `id`: ID dari elemen yang dicari. ID bersifat unik pada dokumen. Tidak boleh terdapat ID yang sama pada dua atau lebih elemen.

_**Return**_

- `Element` object: jika terdapat elemen dengan ID yang dicari.
- `null`: jika tidak terdapat elemen dengan ID yang dicari.

### Contoh

```html
<!DOCTYPE html>

<html>
  <head></head>
  <body>
    <div>
      <p id="paragraph1">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
      </p>
      <p id="paragraph2">
        Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
      </p>
    </div>

    <script>
      let paragraph1 = document.getElementById("paragraph1");
      let paragraph2 = document.getElementById("paragraph2");
      let paragraph3 = document.getElementById("paragraph3");
      console.log(paragraph1); // paragraph1 Element object
      console.log(typeof paragraph1);
      console.log(paragraph2); // paragraph2 Element object
      console.log(typeof paragraph2);
      console.log(paragraph3); // null
      console.log(typeof paragraph3);
    </script>
  </body>
</html>
```

## `Element.innerHTML`

**Mengakses HTML dari Element object**

```html
<html>
  <head></head>
  <body>
    <div>
      <p id="paragraph1">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
      </p>
      <p id="paragraph2">
        Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
      </p>
    </div>

    <script>
      let paragraph1 = document.getElementById("paragraph1");
      let paragraph2 = document.getElementById("paragraph2");
      console.log(paragraph1.innerHTML); // paragraph1 Element object
      console.log(paragraph2.innerHTML); // paragraph2 Element object
    </script>
  </body>
</html>
```

**Melakukan assignment pada innerHTML dari Element object**

```html
<html>
  <head></head>
  <body>
    <div>
      <p id="paragraph1">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
      </p>
      <p id="paragraph2">
        Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
      </p>
    </div>

    <script>
      let paragraph1 = document.getElementById("paragraph1");
      let paragraph2 = document.getElementById("paragraph2");
      paragraph1.innerHTML = "<b>Acong</b> adalah teman dari <b>Djoko</b> dan <b>Sitorus</b>.";
      paragraph2.innerHTML = "<b>Djoko</b> dan <b>Sitorus</b> sangat peduli terhadap <b>Acong</b>.";
    </script>
  </body>
</html>
```

## Event attributes

```html
<html>
  <head></head>
  <body>
    <div>
      <p id="paragraph1">
        <b>Acong</b> adalah teman dari <b>Djoko</b> dan <b>Sitorus</b>.
      </p>
      <p id="paragraph2">
        <b>Djoko</b> dan <b>Sitorus</b> sangat peduli terhadap <b>Acong</b>.
      </p>
      <button id="button1" onclick="button1()">Button 1</button> <!--Cara 1 dengan menuliskan onclick attribute pada element HTML-->
      <button id="button2">Button 2</button>
    </div>

    <script>
      function button1() {
        document.getElementById("paragraph1").innerHTML = '<b>Acong</b> sudah tidak berteman baik dengan <b>Djoko</b> maupun <b>Sitorus</b>.';
      }
      function button2() {
        document.getElementById("paragraph2").innerHTML = 'Persahabatan <b>Acong</b>, <b>Djoko</b> dan <b>Sitorus</b> kandas karena masalah jodoh.';
      }
      let button2Object = document.getElementById("button2");
      button2Object.addEventListener("click", button2); // Cara 2 dengan menggunakan function addEventListener
    </script>
  </body>
</html>
```

[DOM events list](https://developer.mozilla.org/en-US/docs/Web/Events)

## Traversing DOM

### Children

```html
<html>
  <head></head>
  <body>
    <div id="div1">
      <p id="div1_para1">This is div1_para1.</p>
      <button id="div1_button1">This is div1_button1</button>
      <div id="div1_div1">
        <p id="div1_div1_paragraph1">This is div1_div1_paragraph1.</p>
        <button id="div1_div1_button1">This is div1_div1_button1</button>
        <button id="div1_div1_button2">This is div1_div1_button2</button>
      </div>
    </div>

    <script>
      let div1 = document.getElementById("div1");
      console.log('div1 children:');
      for (let i = 0; i < div1.children.length; i++) {
        console.log(div1.children[i].id);
      }
      let div1_div1 = document.getElementById("div1_div1");
      console.log('div1_div1 children:');
      for (let i = 0; i < div1_div1.children.length; i++) {
        console.log(div1_div1.children[i].id);
      }
    </script>
  </body>
</html>
```

### Parent

```html
<html>
  <head></head>
  <body>
    <div id="div1">
      <p id="div1_para1">This is div1_para1.</p>
      <button id="div1_button1">This is div1_button1</button>
      <div id="div1_div1">
        <p id="div1_div1_paragraph1">This is div1_div1_paragraph1.</p>
        <button id="div1_div1_button1">This is div1_div1_button1</button>
        <button id="div1_div1_button2">This is div1_div1_button2</button>
      </div>
    </div>

    <script>
      let div1_div1_button1 = document.getElementById("div1_div1_button1");
      console.log(div1_div1_button1.parentElement.id);
    </script>
  </body>
</html>
```

### Mengakses dan mengubah innerHTML parent dan children

```html
<html>
  <head></head>
  <body>
    <div id="div1">
      <p>Paragraf pertama</p>
      <p>Paragraf kedua</p>
      <p>Paragraf ketiga</p>
      <p>Paragraf keempat</p>
      <button id="button1">Click to bold!</button>
    </div>

    <script>
      function toBold(children) {
        let parent = children.parentElement;
        for (let i = 0; i < parent.children.length; i++) {
          parent.children[i].style.fontWeight = "bold";
        }
      }
      let button1 = document.getElementById("button1");
      button1.addEventListener("click", () => {
        toBold(button1);
      });
    </script>
  </body>
</html>
```

## External JavaScript

Seperti CSS, kode program JavaScript dapat diletakkan pada file eksternal. Kita dapat menyertakan file tersebut pada tag `script`.

`script.js`

```javascript
function toBold(children) {
  let parent = children.parentElement;
  for (let i = 0; i < parent.children.length; i++) {
    parent.children[i].style.fontWeight = "bold";
  }
}
let button1 = document.getElementById("button1");
button1.addEventListener("click", () => {
  toBold(button1);
});
```

`index.html`

```html
<html>
  <head></head>
  <body>
    <div id="div1">
      <p>Paragraf pertama</p>
      <p>Paragraf kedua</p>
      <p>Paragraf ketiga</p>
      <p>Paragraf keempat</p>
      <button id="button1">Click to bold!</button>
    </div>

    <script src="script.js"></script>
  </body>
</html>
```

[**Back to Home**](./../README.md)
