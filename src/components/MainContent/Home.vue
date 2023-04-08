<template>
  <div>
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
      <img class="arrow-down" src="../../assets/Images/down_line.svg" alt="">
    </a>
  </div>
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
  /* top: 40%; */
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

</style>