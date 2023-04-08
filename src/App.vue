<template>
  <div class="container-fluid">
    <header>
      <Header />
    </header>
    <main class="container d-flex flex-wrap">
      <Main />
    </main>
    <footer>
      <Footer />
    </footer>
    <!-- <a class="nav-link switch-theme" href="#">
      <img src="./assets/Images/moon_stars_fill.svg" alt="">
    </a> -->
  </div>
</template>

<script setup>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'
</script>

<style scoped>
.container-fluid {
  padding: 0px;
  min-height: 100vh;
  position: relative;
}

body {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

header {
  height: 60px;
}

main {
  min-height: 100vh;
  /* position: relative; */
}

footer {
  height: 60px;
}

.switch-theme {
  position: absolute;
  top: 95vh;
  right: 25px;
}
</style>
