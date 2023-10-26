<script setup>
const jobs = [
  "Senior Full-Stack Engineer",
  "Senior Designer",
  "Superstar Intern",
];

const { $gsap: gsap } = useNuxtApp();

onMounted(() => {
  gsap.from(".vacancies .heading", {
    scrollTrigger: {
      trigger: ".vacancies .heading",
      scrub: 3,
      start: "top 80%",
      end: "bottom 80%",
    },
    x: -500,
    y: 100,
    opacity: 0,
    duration: 7,
  });
});
</script>

<template>
  <section class="vacancies">
    <div class="heading">Open vacancies</div>

    <div class="row">
      <div class="card" v-for="(job, index) in jobs" :key="index">
        <div class="title">{{ job }}</div>
        <ul>
          <li>Full-time position</li>
          <li>Berlin or remote</li>
          <li>€65-85k, 0.5-1.50% equity share options</li>
        </ul>

        <div class="btn">See details</div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
section {
  width: min(95%, 1480px);
  margin: 0 auto;
  padding: 60px 42px;
}

.heading {
  font-size: 42px;
  font-weight: bold;
  margin-bottom: 48px;
}

.row {
  display: flex;
  gap: 24px;
  flex-wrap: wrap;

  .card {
    padding: 24px;
    background-color: #fefbeb;
    flex: 1 1 250px;
    border-radius: 24px;
    transition: 0.5s ease;
    overflow: hidden;

    .title {
      font-size: 20px;
      font-weight: bold;
      margin-bottom: 8px;
    }

    ul {
      list-style-position: inside;
      li {
        margin-bottom: 8px;
      }
    }

    .btn {
      background-color: #111;
      color: #f5f5f5;
      padding: 0 24px;
      border-radius: 24px;
      width: max-content;
      margin-top: 0px;
      height: 0;
      line-height: 46px;
      transition: 0.25s ease;
    }

    &:hover {
      background-color: #ffefd5;

      .btn {
        margin-top: 24px;
        height: 48px;
      }
    }
  }
}
</style>
