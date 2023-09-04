<template>
    <section class="section testimonial-background my-5 has-text-white">
      <div class="testimonials-container my-5 is-flex is-justify-content-center is-align-content-center is-align-items-center is-align-self-center		 ">
        <div class="navigation my-5">
          <button @click="prevTestimonial" class="ml-5 mr-5 has-text-white is-size-2">&lt;</button>
          <div class="testimonial has-text-centered" style="max-width: 600px; min-width: 200px" v-for="(testimonial, index) in testimonials" :key="index" :class="{ 'active': currentIndex === index }">
            <p class="is-size-5 mb-5">{{ testimonial.quote }}</p>
            <p class="person is-size-6 has-text-weight-semibold">{{ testimonial.person }}</p>
            <p class="title is-size-7 has-text-weight-semibold has-text-white">{{ testimonial.title }}</p>
          </div>
          <button @click="nextTestimonial" class="ml-5 mr-5 has-text-white is-size-2">&gt;</button>
        </div>
      </div>
    </section>
  </template>
  
  <script setup lang="ts">
  import { ref } from 'vue';
  
  const testimonials = [
    {
      quote: "The Southstruct team have a wealth of knowledge and attention to detail in all areas in the concrete construction. We regularly use them for concrete, reinforcement and formwork.",
      person: "SEVE BURGIO",
      title: "OWNER: BURGIO CONSTRUCTION"
    },
    {
      quote: "Southstruct have helped out with various new homes from ground slab, decks and stairs. Southstruct do it all and are a reliable safe team.",
      person: "BRODY HASKELL",
      title: "SUPERVISOR: SUMMIT HOMES"
    },
    {
      quote: "Brilliant job from the team at Southstruct. From the day they quoted it to the day they finished my exposed pool surround. Highly recommend.",
      person: "EVELYN BEC",
      title: "PRIVATE CLIENT"
    },
    {
      quote: "Drew and the team helped design and build a great exposed aggregate alfresco area and double driveway.",
      person: "AARON MONK",
      title: "DIRECTOR: MONK PLUMBING AND GAS"
    },
    {
      quote: "Drew has helped out with a lot of remedial work that pops up in my line of work. Always on time, highest level of quality and very efficient.",
      person: "CONOR DAVIDSON",
      title: "DIRECTOR: TEXTBOOK TILING"
    }
  ];
  
  const currentIndex = ref(0);
  
  const prevTestimonial = () => {
    currentIndex.value = (currentIndex.value - 1 + testimonials.length) % testimonials.length;
  };
  
  const nextTestimonial = () => {
    currentIndex.value = (currentIndex.value + 1) % testimonials.length;
  };
  </script>
