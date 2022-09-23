<template>
  <div class="container">
    <router-view />
  </div>
</template>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400;500;600;700;800&display=swap");

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  outline: none;
}

html {
  scroll-behavior: smooth;
}

body,
html {
  font-family: "Poppins", sans-serif;
}
body {
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 21px;
  font-variant: normal;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  color: white;
  background-color: #000 !important;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  margin-top: 0;
  color: inherit;
}
input {
  outline: 0;
  border: none;
}

ul,
li {
  margin: 0;
  padding: 0;
  list-style: none;
}

button {
  outline: 0;
  border: 0;
}

a {
  font-size: 14px;
  text-decoration: none;
  &:hover {
    text-decoration: none;
  }
}
.container {
  width: 100%;
  margin: 0 auto;
  max-width: 1920px;
  background-image: url("@/assets/appBg.png");

  @media (max-width: 1199px) {
    background-image: none;
  }
}
.slick-dots {
  position: static;

  li {
    width: fit-content !important;
    height: fit-content !important;

    &.slick-active {
      button {
        background-color: gray !important;
      }
    }
    button {
      height: 16px;
      border-radius: 4px;
      width: 15px !important;
      height: 15px !important;
      border-radius: 50% !important;
      background-color: #000 !important;
    }
  }
  @media (max-width: 767px) {
    bottom: -5px !important;
    li {
      &.slick-active {
        button {
          background-color: #e17f00 !important;
        }
      }
      button {
        width: 1.6vw !important;
        height: 1.6vw !important;
      }
    }
  }
}
</style>
