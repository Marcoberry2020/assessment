 <template>
  <nav class="navbar">
    <div class="container">
      <a href="#" class="logo">MySite</a>
      <ul :class="['nav-links', { 'show-menu': isMenuOpen }]">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
      <button class="menu-toggle" @click="toggleMenu">☰</button>
    </div>
  </nav>
</template>

<script lang="ts">
import { ref } from "vue";

export default {
  name: "Navbar",
  setup() {
    const isMenuOpen = ref(false);
    const toggleMenu = () => {
      isMenuOpen.value = !isMenuOpen.value;
    };

    return { isMenuOpen, toggleMenu };
  },
};
</script>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 20px;
  background: linear-gradient(45deg, #ff6b6b, #f06595);
  color: #fff;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
  text-transform: uppercase;
  color: white;
  text-decoration: none;
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 20px;
}

.nav-links a {
  text-decoration: none;
  color: white;
  font-size: 1rem;
  font-weight: 500;
  transition: color 0.3s;
}

.nav-links a:hover {
  color: #ffe66d;
}

.menu-toggle {
  display: none;
  font-size: 1.5rem;
  background: none;
  border: none;
  color: white;
  cursor: pointer;
}

@media screen and (max-width: 768px) {
  .nav-links {
    display: none;
    flex-direction: column;
    position: absolute;
    top: 60px;
    right: 20px;
    background: #f06595;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
    width: 200px;
    padding: 10px;
    z-index: 1000;
  }

  .nav-links.show-menu {
    display: flex;
  }

  .menu-toggle {
    display: block;
  }
}
</style>
