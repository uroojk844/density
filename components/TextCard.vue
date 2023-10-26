<script setup>
let props = defineProps(["card"]);
</script>

<template>
  <div
    class="card" :class="{'rotate':card.rotate}"
    :style="{ 'background-color': card.bg, color: card.text ?? 'black' }"
  >
    <div class="heading">{{ card.heading }}</div>
    <div class="desc">{{ card.desc }}</div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  padding: 48px 32px;
  border-radius: 16px;
  max-width: 300px;

  .heading {
    font-weight: bold;
    margin-bottom: 8px;
  }

  &.rotate {
    transform: rotate(-4deg);
  }

  .desc {
    font-size: 12px;
    line-height: 1.7;
  }
}
</style>
