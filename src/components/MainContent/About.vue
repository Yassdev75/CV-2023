<template>
  <div>
    <div class="container-about d-flex">
      <div class="about-description">
        <h2 class="numbered-heading mb-5">A propos de moi</h2>
        <p>Je suis Yassine, web designer et developpeur web front-end, apres avoir obtenu un bts en negociation relation
          client, je me suis dirigé vers un domaine qui me passionnait vraiment, le domaine du web. J'ai suivis un cursus
          de developpeur web en 2 ans au conservatoire, j'en ai obtenu le diplome en fin 2021 <br><br>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima tempora quod quis libero! Dolore cum nobis,
          earum fuga libero debitis, a aliquid sapiente necessitatibus unde nulla natus iste aspernatur reiciendis!
        </p><br><br>
        <div class="container list-skills">
          <div class="row">
            <div class="col-6">
              <ul class="list-unstyled">
                <li><img src="../../assets/Images/right_small_line.svg" alt="">Html/Css</li>
                <li><img src="../../assets/Images/right_small_line.svg">Javascript</li>
                <li><img src="../../assets/Images/right_small_line.svg">Vuejs</li>
              </ul>
            </div>
            <div class="col-6">
              <ul class="list-unstyled">
                <li><img src="../../assets/Images/right_small_line.svg">Figma</li>
                <li><img src="../../assets/Images/right_small_line.svg">Git/Github</li>
                <li><img src="../../assets/Images/right_small_line.svg">Element 6</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <div>
        <div class="block1"></div>
        <div class="block2"></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {

}
</script>
<style scoped>
/* CSS SECTION A PROPOS */
.container-about {
  margin: 0 130px 0 130px !important;
  gap: 60px;
}

.about-description {
  line-height: 1.3;
  font-size: 1.25rem;
}

.numbered-heading::after {
  content: "";
  display: inline-block;
  position: relative;
  top: -8px;
  width: 200px;
  height: 1px;
  margin-left: 20px;
  background-color: #000000;
}

.block1 {
  width: 300px;
  height: 300px;
  border: solid 2px #000000;
  position: absolute;
  border-radius: 5px;
}

.block2 {
  width: 300px;
  height: 300px;
  top: -15px;
  left: -15px;
  position: relative;
  background: url("../../assets/Images/Pp example.jpg") no-repeat center center/cover;
  border-radius: 5px;
}

.block2:hover {
  background-blend-mode: none;
  filter: none !important;
}

.list-skills {
  line-height: 2;
  font-size: 1rem;
}

@media (max-width: 991px) {
  .container-about {
    margin: 0 !important;
  }
}

</style>