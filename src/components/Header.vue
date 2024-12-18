 <template>
  <header class="header">
    <h1>Echofu paul </h1>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>
</template>

<script lang="ts">
export default {
  name: 'Header',
};
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
  background: #333;
  color: #fff;
}

.header nav ul {
  list-style: none;
  display: flex;
  gap: 1rem;
}

.header nav a {
  color: white;
  text-decoration: none;
}

@media (max-width: 768px) {
  .header {
    flex-direction: column;
    align-items: flex-start;
  }
}
</style>
