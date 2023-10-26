<template>
  <main>
    <NavBar />
    <slot></slot>
    <Footer />
  </main>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;700&display=swap");

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: "Noto Sans JP", sans-serif;
}

a {
  text-decoration: none;
  color: inherit;
}

.primary {
  background-color: #eeeafd;
}
</style>
