<template>
  <div class="container-fluid">
    <header>
      <Header/>
    </header>
    <main class="container d-flex">
      <Main/>
    </main>
    <footer class="bg-dark text-center text-white">
      <Footer/>
    </footer>
  </div>
</template>

<!-- <body> -->
  <!-- Contenu de la page -->
  <!-- <header> -->
    <!-- Contenu de l'en-tête -->
  <!-- </header>
  <nav> -->
    <!-- Contenu de la barre de navigation -->
  <!-- </nav>
  <main> -->
    <!-- Contenu principal de la page -->
  <!-- </main>
  <footer> -->
    <!-- Contenu du pied de page -->
  <!-- </footer>
</body> -->

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
  height: 60px; /* exemple de hauteur */
}

main {
  flex: 1;
  height: calc(100vh - 60px - 100px); /* 60px pour le header, 100px pour le footer */
}

footer {
  height: 100px; /* exemple de hauteur */
}

</style>
