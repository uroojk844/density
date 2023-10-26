<script setup>
const { $gsap: gsap } = useNuxtApp();

const varticalCards = [
  {
    heading: "Learn more about who you are and where you want to go",
    desc: "We ask the right questions to help you better understand why you do things the way you do.",
  },
  {
    heading: "Play and grow together With others on the same journey",
    desc: "Ahead feels like a game, not like a chore, See yourself grow every day towards achieving your goals!",
  },
  {
    heading:
      "Learn about practical skills that you can actually use in real life",
    desc: "We teach you smart psychological techniques and habit-forming strategies that are easy to apply.",
  },
  {
    heading: "Get support that's made for your needs",
    desc: "We build your personal roadmap of lessons and actions towards your goals.",
  },
];

onMounted(() => {
  gsap.from(".workwithus .left", {
    scrollTrigger: {
      trigger: ".workwithus .left",
      scrub: 3,
      start: "top 80%",
      end: "bottom 80%",
    },
    x: -500,
    duration: 5,
  });

  gsap.from(".workwithus .right", {
    scrollTrigger: {
      trigger: ".workwithus .right",
      scrub: 3,
      start: "top 80%",
      end: "bottom 80%",
    },
    x: 500,
    duration: 5,
  });
});
</script>

<template>
  <section class="workwithus">
    <div class="row">
      <div class="heading left">Work with us</div>
      <div class="heading right">ahead</div>
    </div>

    <div class="row">
      <div class="list">
        <div class="card">
          <h2>About</h2>
          <p>
            At ahead our goal is to make self- improvement fun and lasting. We
            know there's a way how to make it work. And that's what aHead is all
            about!
          </p>
        </div>
        <div class="card">
          <h2>Product</h2>
          <p>
            Sure, you could spend ages reading books or sitting in seminars on
            how to become a better spouse, parent, or manager - like we did...
          </p>
        </div>
      </div>

      <div class="vert_scroll">
        <div class="card" v-for="(card, index) in varticalCards" :key="index">
          <h4>{{ card.heading }}</h4>
          <p>
            {{ card.desc }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.workwithus {
  overflow: hidden;
  width: min(95%, 1480px);
  margin: 0 auto;
  padding: 48px;
  background-color: #f4f0ff;
  border-radius: 24px;
  display: grid;
  gap: 48px;
}

.row {
  display: flex;
  justify-content: space-between;
  gap: 24px;
  align-items: flex-start;

  .heading {
    font-size: 36px;
    font-weight: bold;
  }

  .right {
    color: #6341ee;
  }
}

.list {
  max-width: 395px;
  border-radius: 12px;
  overflow: hidden;
  background-color: #fff;

  .card {
    padding: 24px;

    &:last-child {
      background-color: #fcf6f0;
      border-radius: 12px 12px 0 0;
    }
  }

  h2 {
    margin-bottom: 4px;
  }

  p {
    color: #333;
    line-height: 1.8;
  }
}

.vert_scroll {
  width: 400px;
  max-height: 500px;
  overflow-y: auto;
  display: grid;
  gap: 16px;
  align-items: flex-start;

  &::-webkit-scrollbar {
    width: 8px;
    background-color: white;
    border-radius: 4px;
  }

  &::-webkit-scrollbar-thumb {
    border-radius: 4px;
    background-color: #b2a1ec;
  }

  .card {
    background-color: #fff;
    padding: 24px;
    border-radius: 12px;
    max-width: 320px;

    h4 {
      margin-bottom: 8px;
    }

    p {
      font-size: 14px;
    }
  }
}
</style>
