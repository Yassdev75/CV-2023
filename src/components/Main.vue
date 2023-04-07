<template>
  <!-- PRESENTATION -->
  <section class="section-part w-100 d-flex justify-content-center align-items-center text-uppercase">
    <div>
      <h1>Hey, je suis Yassine Zambib</h1>
      <div id="text-container">
        <span id="typed-text"></span><span id="blink">_</span>
      </div>
      <p class="pt-3 text-muted">Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi suscipit sequi quod nihil sapiente maiores, dolorum repellat eligendi asperiores nisi. Labore aut minima amet repellat animi assumenda dicta reiciendis recusandae.</p>
    </div>
  </section>
  <!-- MES EXPERIENCES -->
  <section class="section-part">
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
.section-part {
  height: calc(100vh - 60px);
  margin: 0px !important;
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
</style>