<template>
  <nav class="navbar navbar-expand-lg navbar-transparent p-lg-4">
    <a class="navbar-brand" href="#">
      <img class="logo-site animate__animated animate__bounceInLeft" src="../../public/Favicon.svg" alt="Logo site">
    </a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav"
      aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
      <ul class="navbar-nav animate__animated animate__bounceInRight">
        <li class="nav-item active">
          <a class="nav-link" href="#">EN<span class="sr-only"></span></a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">
            <img src="../assets/Images/mail_fill.svg" alt="">
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">
            <img src="../assets/Images/linkedin_fill.svg" alt="">
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">
            <img src="../assets/Images/dribbble_fill.svg" alt="">
          </a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  
}
</script>

<style scoped>
.logo-site {
  height: 36px;
  width: 36px;
}
</style>