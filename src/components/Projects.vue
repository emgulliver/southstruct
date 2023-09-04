<template>
  <section class="section">
    <h2 class="has-text-centered is-size-3 mb-5">OUR PROJECTS</h2>
    <div class="projects-container">
      <div class="project-card" v-for="(project, index) in projects" :key="index">
        <div class="project-image" @mouseover="showOverlay(index)" @mouseout="hideOverlay">
          <img :src="project.src" :alt="project.heading" />
          <div class="overlay" v-if="overlayIndex === index"></div>
        </div>
        <div class="project-content">
          <p class="project-heading">{{ project.heading }}</p>
          <p class="project-paragraph">{{ project.title }}</p>
        </div>
      </div>
    </div>
  </section>
</template>


  
  <script setup lang="ts">
import ResidentialPalmyra from '../../public/ResidentialPalmyra.jpg';
import ResidentialCoogee from '../../public/ResidentialCoogee.jpg';
import RockinghamCarpark from '../../public/RockinghamCarpark.jpg';
import CoogeeApartments from '../../public/CoogeeApartments.jpg';
import CoogeeResidential from "../../public/CoogeeResidential.jpg";
import MarbleBar from "../../public/MarbleBar.png";
import Inglewood from "../../public/Inglewood.jpg";
import Melville from "../../public/Melville.jpg";



  const projects = [
    {
      src: ResidentialPalmyra,
      heading: "RESIDENTIAL PALMYRA",
      title: "HONED, SEAMLESS POOL SURROUNDING",
    },
    {
      src: ResidentialCoogee,
      heading: "RESIDENTIAL COOGEE",
      title: "EXPOSED AGGREGATE TO DOUBLE DRIVEWAY",
    },
    {
      src: RockinghamCarpark,
      heading: "ROCKINGHAM CARPARK",
      title: "LIGHT NON-SKID FINISH FOR CARPARK",
    },
    {
      src: CoogeeApartments,
      heading: "COOGEE APARTMENTS",
      title: "EXCAVATION & REINFORCEMENT TO FOUNDATIONS",
    },
    {
      src: CoogeeResidential,
      heading: "COOGEE RESIDENTIAL",
      title: "FORMWORK REINFORCEMENT TO SUSPENDED DECK",
    },
    {
      src: MarbleBar,
      heading: "MARBLE BAR HIGHWAY EXTENSION",
      title: "FORM, REINFORCE, POUR HEADWALL FOUNDATION & WALLS",
    },
    {
      src: Inglewood,
      heading: "INGLEWOOD AGED CARE FACILITY",
      title: "FORMWORK REINFORCEMENT & CONCRETE TO LOAD BEARING COLUMN",
    },
    {
      src: Melville,
      heading: "CITY OF MELVILLE",
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
  
