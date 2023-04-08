<template>
  <!-- PRESENTATION -->
  <section class="section-home w-100 d-flex justify-content-center align-items-center text-uppercase">
    <div>
      <h1 class="animate__animated animate__fadeInDown">Hey, je suis Yassine Zambib</h1>
      <div id="text-container">
        <span id="typed-text"></span><span id="blink">_</span>
      </div>
      <p class="pt-3 text-muted animate__animated animate__fadeInUp">Lorem ipsum dolor sit amet consectetur adipisicing
        elit. Modi suscipit sequi quod nihil sapiente maiores, dolorum repellat eligendi asperiores nisi. Labore aut
        minima amet repellat animi assumenda dicta reiciendis recusandae.</p>
    </div>
    <a class="text-light arrow-container" href="#content">
      <img class="arrow-down" src="../assets/Images/down_line.svg" alt="">
    </a>
  </section>
  <!-- A PROPOS -->
  <section class="section-about container w-100 d-flex align-items-center">
    <div class="container-about d-flex">
      <div>
        <h2 class="numbered-heading mb-5">A propos de moi</h2>
        <p>Je suis Yassine, web designer et developpeur web front-end, apres avoir obtenu un bts en negociation relation
          client, je me suis dirigé vers un domaine qui me passionnait vraiment, le domaine du web. J'ai suivis un cursus de
          developpeur web en 2 ans au conservatoire, j'en ai obtenu le diplome en fin 2021</p>
      </div>
      <div>
        <div style="width: 300px; height: 300px; border: solid 1px black"></div>
      </div>
    </div>
  </section>
  <!-- PRESENTATION -->
  <section>
  </section>
</template>

<script>
export default {

}

document.addEventListener("DOMContentLoaded", function () {
  const typedText = document.querySelector('#typed-text');
  const text = "Je suis un UI/UX Designer & front-end web developer";

  function typeWriter(text, i) {
    typedText.textContent += text.charAt(i);
    i++;
    setTimeout(function () {
      typeWriter(text, i);
    }, 50);
  }

  typeWriter(text, 0);
});

</script>

<style scoped>
.section-about,
.section-home {
  height: calc(100vh - 60px);
  margin: 0px !important;
}

/* CSS SECTION HOME */

.section-home {
  position: relative;
}

.arrow-container {
  position: absolute;
  top: 80%;
  left: 45%;
}

h1 {
  font-size: 3.5rem;
}

#typed-text {
  font-size: 2rem;
}

/* CSS CODE CLIGNONANT */
#blink {
  animation: blink-animation 1s infinite;
}

@keyframes blink-animation {
  50% {
    opacity: 0;
  }
}

/* CSS FLECHE SCROLL */

@keyframes blink {
  50% {
    opacity: 0.5;
  }
}

.arrow-down {
  animation: blink 1.5s ease-in-out infinite;
  height: 52px;
}

/* CSS SECTION A PROPOS */
.container-about {
  margin: 0 130px 0 130px;
  gap: 50px;
}

.numbered-heading::before {
  position: relative;
  bottom: 4px;
  counter-increment: section 1;
  content: "0" counter(section) ".";
  margin-right: 10px;
  color: var(--green);
  font-family: var(--font-mono);
  font-size: clamp(var(--fz-md), 3vw, var(--fz-xl));
  font-weight: 400;
}

.numbered-heading::after {
  content: "";
  display: inline-block;
  position: relative;
  top: -8px;
  width: 300px;
  height: 1px;
  margin-left: 20px;
  background-color: #000000;
}
</style>