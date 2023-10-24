<template>
  <main>
    <NavBar />
    <slot></slot>
  </main>
</template>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: Arial, Helvetica, sans-serif;
}

a {
  text-decoration: none;
  color: inherit;
}

.primary {
  background-color: #eeeafd;
}
</style>
