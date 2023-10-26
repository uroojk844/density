<script setup>
const { $gsap: gsap } = useNuxtApp();

onMounted(() => {
  gsap.from("#meetApp .scale", {
    scrollTrigger: {
      trigger: "#meetApp .scale",
      scrub: 3,
      start: "top 80%",
      end: "bottom 80%",
    },
    x: "-20%",
    scale: 0.3,
    duration: 2,
  });

  gsap.from("#meetApp .logo", {
    scrollTrigger: {
      trigger: "#meetApp .logo",
      scrub: 3,
      start: "top 90%",
      end: "bottom 90%",
    },
    transform: "scale(0.3) rotate(-90deg)",
    duration: 2,
  });
});
</script>

<template>
  <section class="row" id="meetApp">
    <div class="col left">
      <div class="desc scale">Built out of frustration</div>
      <div class="heading scale">Meet the ahead app</div>
      <div class="logo scale">
        <img src="@/assets/img/logo.jpg" alt="logo" />
      </div>
    </div>
    <div class="col right">
      <p class="scale">
        A personalized pocket coach that provides bite- sized, science-driven
        tools to boost emotional intelligence.
      </p>
      <p class="scale">
        Think of it as a pocket cheerleader towards a better, more fulfilling.
      </p>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.row {
  width: min(95%, 1480px);
  margin: 0 auto;
  padding: 24px;
  background-color: #fcf6f0;
  min-height: 83vh;
  border-radius: 24px;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
}

.logo {
  display: grid;
  place-items: center;
  width: 220px;
  aspect-ratio: 1;
  background-color: #fff;
  border: 10px solid #f7f7f7;
  border-radius: 50%;
  margin-left: 10%;

  img {
    width: 60px;
    mix-blend-mode: multiply;
  }
}

.left {
  padding: 32px;
  display: grid;
  align-content: center;
  .desc {
    margin-bottom: 8px;
  }

  .heading {
    font-size: 40px;
    font-weight: bold;
    margin-bottom: 16px;
  }
}

.right {
  display: grid;
  place-content: center;
  gap: 16px;

  p {
    line-height: 1.5;
    max-width: 450px;
    font-size: 20px;
    color: #555;
  }
}
</style>
