<template>
  <section class="column">
    <div class="heading">EQ beats IQ</div>
    <p>
      People with high emotional intelligence (EQ) live more fulfilled lives.
      They tend to be happier and have healthier relationships.
    </p>
    <p>
      They are more successful in their pursuits and make for inspiring leaders.
      According to science, they earn $29k a year.
    </p>
  </section>
</template>

<style scoped>
.column {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
  gap: 32px;
  max-width: max-content;
  margin: 0 auto;
  height: 350px;
  align-content: center;
  padding: 16px;
}

.heading {
  font-size: 28px;
  font-weight: bold;
}

.column p {
  color: #555;
  font-size: 24px;
  line-height: 1.5;
}
</style>
