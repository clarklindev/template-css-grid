## Run example

- open with live-server

## font size

- set base font size on body
- set headers h1-h6 as rem values
- in @media query, update the body default font-size, then everything else using rem is updated according to default font-size.

```css
body {
  font-size: 16px;
}

h1,
h3 {
  font-size: 1.2rem;
}

@media screen and (min-width: 620px) {
  body {
    font-size: 18px;
  }
}

@media screen and (min-width: 960px) {
  font-size: 20px;
}

@media screen and (min-width: 1200px) {
  font-size: 22px;
}
```

<!-- ---------------------------------------------------------------------------------------- -->

## font-famiy

- define font using @font-face
- then src tag
- reference it in css via font-family name

```css
body {
  font-family: 'Rubic Regular';
}
@font-face {
  font-family: 'Rubic Regular';
  src: url('assets/fonts/Rubic-Regular.ttf');
}
```

## css grid

```css
- grid-area: <grid-row-start> / <grid-column-start> / <grid-row-end> / <grid-column-end>
- grid-area: 1/2/1/3;

OR

- grid-column: <start column> / <end column>
- grid-column: 1/3

OR

- grid-column-start:
- grid-column-end:
```

<!-- ---------------------------------------------------------------------------------------- -->

## css grid-template-areas

```html
<div class="example3">
  <main>main</main>
  <section class="yum">yum</section>
  <header>header</header>
  <section class="candy">candy</section>
  <section class="nom">nom</section>
  <footer>footer</footer>
</div>
```

```css
.example3 {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);
  grid-template-areas:
    'main main header'
    'main main candy'
    'nom yum candy'
    'footer footer candy';
}

section.yum {
  grid-area: yum;
  background: blue;
}
```
