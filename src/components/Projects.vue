<template>
  <section class="section">
    <h2 class="has-text-centered is-size-3 mb-5">OUR PROJECTS</h2>
    <div class="projects-container columns is-multiline mt-5">
      <div class="column is-4" v-for="(project, index) in projects" :key="index">
        <div class="card">
          <div class="card-image" @mouseover="showOverlay(index)" @mouseout="hideOverlay">
            <figure class="image">
              <img :src="project.src" :alt="project.heading" style="height: 100%;"/>
            </figure>
            <div class="overlay" v-if="overlayIndex === index"></div>
          </div>
          <div class="card-content">
            <p class="project-heading">{{ project.heading }}</p>
            <p class="project-title">{{ project.title }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>



  
  <script setup lang="ts">
  const projects = [
    {
    src: "../../public/ResidentialPalmyra.jpg",
      heading: "Residential Palmyra",
      title: "HONED, SEAMLESS POOL SURROUNDING",
    },
    {
        src: "../../public/ResidentialCoogee.jpg",
      heading: "RESIDENTIAL COOGEE",
      title: "EXPOSED AGGREGATE TO DOUBLE DRIVEWAY",
    },
    {
        src: "../../public/RockinghamCarpark.jpg",
      heading: "ROCKINGHAM CARPARK",
      title: "LIGHT NON-SKID FINISH FOR CARPARK",
    },
    {
        src: "../../public/CoogeeApartments.jpg",
      heading: "COOGEE APARTMENTS",
      title: "EXCAVATION & REINFORCEMENT TO FOUNDATIONS",
    },
    {
        src: "../../public/CoogeeResidential.jpg",
      heading: "COOGEE RESIDENTIAL",
      title: "FORMWORK REINFORCEMENT TO SUSPENDED DECK",
    },
    {
        src: "../../public/MarbleBar.png",
      heading: "MARBLE BAR HIGHWAY EXTENSION",
      title: "FORM, REINFORCE, POUR HEADWALL FOUNDATION & WALLS",
    },
    {
        src: "../../public/Inglewood.jpg",
      heading: "INGLEWOOD AGED CARE FACILITY",
      title: "FORMWORK REINFORCEMENT & CONCRETE TO LOAD BEARING COLUMN",
    },
    {
        src: "../../public/Melville.jpg",
      heading: "RESIDENTIAL COOGEE",
      title: "DEMOLITION & REINSTATEMENT OF FOOTPATH",
    },

  ];
  
  let overlayIndex: any = null;
  
  const showOverlay = (index: any) => {
    overlayIndex = index;
  };
  
  const hideOverlay = () => {
    overlayIndex = null;
  };
  
  </script>
  
