<template>
  <div class="container-fluid">
    <header>
      <Header/>
    </header>
    <main class="container d-flex flex-wrap">
      <Main/>
    </main>
    <footer>
      <Footer/>
    </footer>
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
  /* flex: 1; */
  min-height: 100vh;
  /* height: calc(100vh - 60px - 60px); */
}

footer {
  height: 60px;
}

</style>
