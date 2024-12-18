 <template>
  <div id="app">
    <Header />
    <main class="container">
      <Home />
    </main>
    <Footer />
  </div>
</template>

<script lang="ts">
import Header from './components/Header.vue';
import Home from './components/Home.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Home,
    Footer,
  },
};
</script>

<style>
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
main {
  flex: 1;
}
</style>
