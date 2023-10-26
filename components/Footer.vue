<template>
  <footer>
    <img src="@/assets/img/logo.jpg" alt="logo" />
    <h1>ahead</h1>

    <div class="row">
      <div class="addr">
        <img
          width="24"
          height="24"
          src="https://img.icons8.com/ios-filled/50/marker.png"
          alt="marker"
        />
        Auguststraße 26, 10117 Berlin
      </div>
      <a href="mailto:hi@ahead-app.com" class="mail"
        ><img
          width="24"
          height="24"
          src="https://img.icons8.com/ios-filled/50/circled-envelope.png"
          alt="circled-envelope"
        />
        hi@ahead-app.com</a
      >
    </div>

    <img class="appstore" src="@/assets/img/appstore.webp" alt="appstore" />
  </footer>
</template>

<style lang="scss" scoped>
footer {
  border-top: 3px solid #efefef;
  padding: 48px 0;
  text-align: center;

  img {
    max-width: 80px;
  }

  h1 {
    color: #6142e6;
  }

  .appstore {
    max-width: 180px;
  }

  .row {
    display: flex;
    justify-content: center;
    gap: 48px;
    flex-wrap: wrap;
    padding: 24px 0;

    .mail, .addr {
        display: flex;
        align-items: center;
        gap: 8px;
    }
  }
}
</style>
