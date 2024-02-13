@use "cssReset";

$font-family-primary: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
$font-family-secondary: "Roboto", sans-serif;
$font-size: 16px;
$font-weight: 400;
$line-height: 1.5;
$color-off-white: #fdfbf9;
$color-black: #0d0a06;
$color-sand: #e9e5e1;
$color-beige: #ece5db;
$color-cafe-lette: #ceb68f;
$border-radius: 8px;

.visually-hidden {
clip: rect(0 0 0 0);
clip-path: inset(50%);
height: 1px;
overflow: hidden;
position: absolute;
white-space: nowrap;
width: 1px;
}

@mixin background-image($url) {
  background-image: url($url);
background-repeat: no-repeat;
background-size: cover;
}

@mixin circle {
border-radius: 50%;
aspect-ratio: 1 / 1;
}
@mixin image-cover {
object-fit: cover;
}

@mixin display-flex($flex-direction, $justify-content, $align-items, $gap) {
display: flex;
flex-direction: $flex-direction;
justify-content: $justify-content;
align-items: $align-items;
gap: $gap;
}

main {
background-color: $color-beige;
}
header {
position: fixed;
background-color: $color-beige;
z-index: 10;
width: 100%;
nav {
@include display-flex(row, space-between, center, 0.5rem);
img {
height: 40px;
width: auto;
}
}
img {
height: 40px;
width: auto;
}
}

.hero {
height: 55svh;
video {
width: 100%;
height: 100%;
object-fit: cover;
}
}

.offers {
padding: 6rem 4rem;
.offer-grid {
display: grid;
grid-template-columns: repeat(12, 1fr);
grid-template-rows: 10svh 20svh;
grid-column-gap: 20px;
grid-row-gap: 20px;

    .offer-box1 {
      grid-area: 1 / 4 / 2 / 10;

      background-color: red;
    }
    .offer-box2 {
      grid-area: 2 / 4 / 3 / 7;
      object-fit: cover;
      background-color: blue;
    }
    .offer-box3 {
      grid-area: 2 / 7 / 3 / 10;
      object-fit: cover;
      background-color: green;
    }
    .offer-box4 {
      grid-area: 1 / 1 / 3 / 4;
      object-fit: cover;
      background-color: yellow;
    }
    .offer-box5 {
      grid-area: 1 / 10 / 3 / 13;
      object-fit: cover;
      background-color: orange;
    }

}
}

.info {
width: 100svw;
padding: 1rem 4rem;
text-align: center;
.info-con {
@include display-flex(row, space-around, center, 0);

    .info-box {
      img {
        @include circle();
        object-fit: cover;
        width: 120px;
      }
    }

}
}
.cases {
padding: 4rem 6rem;
.cases-container {
display: grid;
grid-template-columns: repeat(12, 1fr);
grid-template-rows: repeat(4, 1fr);
grid-column-gap: 20px;
grid-row-gap: 20px;

    .cb1 {
      grid-area: 1 / 4 / 2 / 10;
      background-color: red;
    }
    .cb2 {
      grid-area: 2 / 4 / 3 / 7;
      background-color: blue;
    }
    .cb3 {
      grid-area: 2 / 7 / 3 / 10;
      background-color: green;
    }
    .cb4 {
      grid-area: 1 / 1 / 3 / 4;
      background-color: yellow;
    }
    .cb5 {
      grid-area: 1 / 10 / 3 / 13;
      background-color: orange;
    }
    .cb6 {
      grid-area: 3 / 1 / 5 / 7;
      background-color: pink;
    }
    .cb7 {
      grid-area: 3 / 7 / 4 / 13;
      background-color: purple;
    }
    .cb8 {
      grid-area: 4 / 7 / 5 / 13;
      background-color: $color-cafe-lette;
    }

}
}

.kontakt-formular {
height: 40svh;
background-color: $color-black;
@include display-flex(column, center, center, 0);

h3 {
font-size: 2rem;
color: $color-off-white;
}

p {
font-size: 1.2rem;
color: $color-off-white;
}

.email-submit {
@include display-flex(row, space-around, center, 0);
background-color: $color-off-white;
margin-top: 0.5rem;

    .mail {
      border: 1px solid $color-black;
      // border-left: 1px solid $color-black;
      // border-top: 1px solid $color-black;
      // border-bottom: 1px solid $color-black;
      width: 250px;
      height: 30px;
    }
    .submit {
      width: 120px;
      border: 1px solid $color-black;
      height: 30px;
      text-align: center;
    }

}
}
