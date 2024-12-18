<template>
  <footer class="footer">
    <p>echofu paul; 2024 My Vue App. All rights reserved.</p>
  </footer>
</template>

<script lang="ts">
export default {
  name: 'Footer',
};
</script>

<style scoped>
.footer {
  text-align: center;
  padding: 1rem;
  background: #333;
  color: #fff;
}

@media (max-width: 768px) {
  .footer {
    font-size: 0.875rem;
  }
}
</style>
