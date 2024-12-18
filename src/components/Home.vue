<template>
  <section class="home">
    <div class="hero">
      <h1>Welcome to My Vue App</h1>
      <p>Building responsive sites is easy with Vue and TypeScript.</p>
    </div>
  </section>
</template>

<script lang="ts">
export default {
  name: 'Home',
};
</script>

<style scoped>
.hero {
  text-align: center;
  padding: 2rem;
}

@media (max-width: 768px) {
  .hero {
    padding: 1rem;
  }
}
</style>
