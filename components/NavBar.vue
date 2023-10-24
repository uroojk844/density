<template>
  <header>
    <nav>
      <NuxtLink to="/"
        ><img
          src="https://www.stockvault.net/data/2018/06/05/252340/preview16.jpg"
          class="logo"
      /></NuxtLink>
      <div class="content">
        <NuxtLink to="/" class="nav-links">Emotions</NuxtLink>
        <NuxtLink to="/" class="nav-links">Manifesto</NuxtLink>
        <NuxtLink to="/" class="nav-links">Self awerness test</NuxtLink>
        <NuxtLink to="/" class="nav-links">Work with us</NuxtLink>
      </div>
      <div class="btn">Download App</div>
    </nav>
  </header>
</template>

<style scoped>
header {
  position: sticky;
  top: 0;
  width: 100%;
  background-color: #fff;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1400px;
  margin: 0 auto;
  padding: 16px;
}

.logo {
  max-width: 60px;
}

img {
  width: 100%;
}

.content {
  display: flex;
  gap: 48px;
}

.nav-links {
  white-space: nowrap;
}

.btn {
  background: #111;
  color: #f5f5f5;
  border-radius: 24px;
  padding: 12px 24px;
}
</style>
