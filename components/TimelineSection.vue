<script setup>
const { $gsap: gsap } = useNuxtApp();

onMounted(() => {
  gsap.from(".timeline-section", {
    scrollTrigger: {
      trigger: ".timeline-section",
      scrub: 3,
      start: "top 80%",
      end: "bottom 80%",
    },
    x: -600,
    y: 100,
    duration: 3,
  });
});

const events = ref([
  {
    heading: "It's not as easy as 1-2-3.",
    desc: "The journey of change may be long, but our sessions are quick. We get to the point and tell you what you want to know (and nothing else).",
  },
  {
    heading: "Old habits are hard to break.",
    desc: "And bad behaviors die hard. Fortunately, we give you great, science-backed techniques to use.",
  },
  {
    heading: "You and your motivation don't have a long-term relationship.",
    desc: "Luckily, we can proactively prepare you for the marathon, not just the race. Effective, memorable exerciseswill help you stick to your goals.",
  },
]);
</script>

<template>
  <section class="timeline-section">
    <div class="desc">Wrong with self-improvement & how we're fixing it.</div>
    <div class="heading">Self-improvement. Ugh.</div>
  </section>

  <v-container style="max-width: 700px">
    <v-timeline side="end" align="start" truncate-line="both">
      <v-timeline-item
        v-for="(item, index) in events"
        :key="index"
        dot-color="#6948f0"
        size="x-small"
      >
        <h1 class="text-h5 font-weight-bold mb-2">{{ item.heading }}</h1>
        <p class="mb-8" style="line-height: 1.8">{{ item.desc }}</p>
      </v-timeline-item>
    </v-timeline>
  </v-container>
</template>

<style lang="scss" scoped>
.timeline-section {
  width: min(95%, 1480px);
  margin: 0 auto;
  padding: 48px 0;

  .desc {
    margin-bottom: 8px;
  }

  .heading {
    font-size: 42px;
    font-weight: bold;
  }

  .timeline-card {
    h1 {
      margin-bottom: 16px;
    }
    p {
      line-height: 1.5;
    }
  }
}
</style>
