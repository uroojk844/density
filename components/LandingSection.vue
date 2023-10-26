<template>
  <section class="landing primary">
    <div class="content">
      <p>Ahead app</p>
      <div class="jumbo">Master your life by mastering emotions</div>
      <img
        class="btn"
        src="@/assets/img/appstore.webp"
        alt="download on appstore"
      />
    </div>
    <div class="phone">
      <img
        src="https://help.apple.com/assets/64067987823C71654C27CD1A/64067990823C71654C27CD47/en_US/b437baddff8dfb99e9192e449bafa656.png"
        alt="phone"
      />
    </div>
  </section>
</template>

<style scoped>
.landing {
  min-height: 83vh;
  display: grid;
  grid-template-columns: 1fr 1fr;

  max-width: 1480px;
  margin: 0 auto;
  padding: 60px;
  border-radius: 60px;
}

.content {
  display: grid;
  align-content: center;
  gap: 16px;
}

.jumbo {
  font-size: 60px;
  font-weight: bold;
  max-width: 500px;
}

.btn {
  max-width: 200px;
}

img {
  width: 100%;
}

.phone {
  display: grid;
  place-items: center;
}

.phone img {
  width: 220px;
}
</style>
