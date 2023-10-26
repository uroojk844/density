<script setup>
const { $gsap: gsap } = useNuxtApp();

let animCards;

onMounted(() => {
  let tl = gsap.timeline();

  tl.from("h1", {
    scrollTrigger: {
      trigger: "h1",
      scrub: 3,
      start: "top 90%",
      end: "bottom 90%",
    },
    x: -500,
    fontSize: 12,
    duration: 2,
  });

  tl.to(".card", {
    scrollTrigger: {
      trigger: ".card",
      scrub: 7,
      start: "top 80%",
      end: "bottom 50%",
    },
    transform: "translateX(-500px)",
    duration: 3,
  });
});

let cards = [
  {
    heading: "You argue with a colleague",
    desc: "You get angry and defensive, instead of staying open and working towards common ground.",
    bg: "#eeeafd",
  },
  {
    heading: "You get a promotion at work",
    desc: "You question yourself and wonder when they'll realize you're an unqualified imposter, instead of trusting yourself & your abilities.",
    bg: "#6240ef",
    text: "white",
    rotate: true,
  },
  {
    heading: "You attend a class reunion",
    desc: "You compare yourself with your peers'achievements, instead of making yourself-judgement more independent of others.",
    bg: "#ffefd5",
  },
  {
    heading: "You are at a lively dinner party",
    desc: "You play  on your phone, instead Ofconfidently approaching strangers and striking up a chat.",
    bg: "#fefbeb",
  },
  {
    heading: "You hit dead end in a negotiation",
    desc: "You get nervous, frazzled, and frustrated, instead of staying optimistic and solution-oriented.",
    bg: "#f1f8f7",
  },
];
</script>

<template>
  <section>
    <h1>Does this sound familiar...</h1>
    <div class="scroll">
      <TextCard v-for="(card, index) in cards" :key="index" :card="card" />
    </div>
  </section>
</template>

<style lang="scss" scoped>
section {
  padding: 24px;
}

h1 {
  margin-bottom: 42px;
  font-size: 42px;
}

.scroll {
  display: grid;
  grid-auto-flow: column;
  grid-auto-columns: max-content;
  justify-content: start;
  align-items: center;
  gap: 32px;
  padding: 24px 0;
  overflow-x: auto;

  &::-webkit-scrollbar {
    display: none;
  }
}
</style>
