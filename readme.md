# Perkenalan Sass

* Apa itu Sass?
Sass itu sebuah css preprocessor. Preprocessor sendiri adalah sebuah compiler. Jadi Sass itu membuat bahasa sendiri yang bertujuan untuk menyerderhanakan, memodulkan, dan membuatnya menjadi lebih teratur.

* Kenapa Sass?
Sass ada lebih dulu, memiliki banyak komunitas, dan lebih fleksibel untuk project yang kompleks.

* Bagaimana cara menggunakan Sass?
Langkah pertama adalah menginstalnya lebih dulu di komputer. Bisa dilihat di sass-lang.com. Gunakan versi Nodejs jangan gunakan versi Ruby. Kenapa versi Nodejs, karena nanti kita akan banyak menggunakan tools dari Nodejs.

## Instal Sass

Sebelum instal sass pastikan nodejs sudah terpasang. Untuk yang lebih mahir, gunakan nvm agar bisa menginstal lebih dari satu veri nodejs.

[nvm](https://github.com/creationix/nvm)<br />
[nodejs](https://nodejs.org/)<br />
[node sass](https://github.com/sass/node-sass)<br />

```
npm install node-sass 
sudo npm install node-sass (linux)
```

## Fitur Sass

1. Variables
```
// Base name color
$black: #000
$dark-grey: lighten($black, 20%);
$grey: lighten($black, 40%);
// Base variables
$base-width: 400px;
$base-font-size: 1em;
$base-font-color: $dark-grey;
$secondary-font-color: $grey;
```
2. Nesting
```
.class {
	font-color: $base-font-color;
	.subclass { font-color: $secondary-font-color;}
}
```
3. Partials
```
_partial.scss
@import 'partial';
```
4. Import
```
_partial.scss
@import 'partial';
```
5. Mixins
```
@mixin border-radius($radius) {
  -webkit-border-radius: $radius;
     -moz-border-radius: $radius;
      -ms-border-radius: $radius;
          border-radius: $radius;
}
.box { @include border-radius(10px); }
```
6. Extend
```
.background-grey { background: $grey;}
.box { @extend .background-grey;}
.wrapper { @extend .background-grey;}
```
7. Operators
```
.entry-title { font-size:  $base-font-size * 2;}
```

## Kompilasi Sass

Untuk kompilasi sass gunakan sintaks di bawah dan jalankan di terminal

```
sass input.scss output.css
```

Untuk kompilasi otomatis gunakan sintaks di bawah dan jalankan di terminal

```
sass --watch input.scss:output.css
```

Atau gunakan aplikasi untuk kompilasi secara otomatis seperti beberapa perangkat lunak berikut

1. Codekit (berbayar)
2. Compass.app (berbayar dan open source)
3. Hammer (berbayar)
4. Koala (open source)
5. LiveReload (berbayar dan open source)
6. Mixture (gratis)
7. Prepros (berbayar)
8. Scout (open source)

Untuk penggunaan lebih mahir dengan kebutuhan yang lebih kompleks saya menyarankan untuk menggunakan Grunt atau Gulp.