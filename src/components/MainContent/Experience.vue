<template>
  <div class="container-experience d-flex">
    <div class="experience-description">
      <h2 class="numbered-heading mb-5">Mes experiences</h2>
      <div class="container">
        <!-- ---------- -->
        <div class="row">
          <div class="col-md-4 d-flex align-items-center">
            <ul>
              <li v-for="(section, index) in sections" :key="index" :class="{ active: section.isActive }"
                @click="updateCurrentSection(index)">
                {{ section.title }}
              </li>
            </ul>
          </div>
          <div class="col-md-8 d-flex align-items-center content-container">
            <div class="content">
              <h2 class="mb-3">{{ currentSection.title }}</h2>
              <p>{{ currentSection.content }}</p>
            </div>
          </div>
        </div>
        <!-- ---------- -->
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      sections: [
        {
          title: 'Cowork.id',
          content: 'Stage de fin de ma premiere année d etude au sein d une entreprise a station f en 2019 du nom de coworkid, mes taches etaient nanani nanana',
          isActive: true
        },
        {
          title: 'Hackaton',
          content: 'Lors d un hackaton organise avec l ecole j ai pue participer a la creation d un site internet pour la journee de la femme, l objectif venir en aide a ces femmes entrepreneurs, celle a qui j ai pu venir en aide voulait ameliorer les aspects front de son site venant en aide aux etudiants etranger',
          isActive: false
        },
        {
          title: 'Bubble plan',
          content: 'Mon experience la plus longue en alternance durant ma deuxieme annee d etude, j ai lors de ce contrat d un an pu ameliorer mes capiciter en front mais egalement en design blablablablablablablablablablablablablablablablabla',
          isActive: false
        }
      ],
      currentSection: {
        title: 'Cowork.id',
        content: 'Stage de fin de ma premiere année d etude au sein d une entreprise a station f en 2019 du nom de coworkid, mes taches etaient nanani nanana'
      },
    };
  },
  methods: {
    updateCurrentSection(index) {
      this.sections.forEach((section) => {
        section.isActive = false; // Réinitialiser la propriété isActive pour tous les éléments
      });
      this.sections[index].isActive = true; // Définir la propriété isActive sur true pour l'élément sélectionné
      this.currentSection = this.sections[index];
    },
  },
};
</script>

<style scoped>
ul {
  list-style-type: none;
  padding: 0;
  border-left: solid 3px #90b1ae;
}

li {
  cursor: pointer;
  padding: 10px 0;
  text-align: center;
  width: 120%;
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
}

ul>li:hover {
  /* color: #d3f7f3; */
  background-color: #778787;
  transition: background-color 1.5s ease;
}

.active {
  color: #d3f7f3;
  background-color: #000000;
  /* border-left: solid 4px #262d2c; */
  transition: background-color 1s ease;
}

.content {
  padding: 20px;
}

.content-container {
  min-height: 300px;
}

.container-experience {
  margin: 0 230px 0 230px;
  /* gap: 60px; */
}

.experience-description {
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

@media (max-width: 992px) {
  .container-experience {
    margin: 0 50px 0 50px;
  }
}
@media (max-width: 757px) {
  .container-experience {
    margin: 0px;
  }
}
</style>