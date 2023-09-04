<template>
  <section class="footer has-background-dark has-text-light">
 <div class="container mt-5" style="max-width: 1000px;">
  <div class="columns">
        <!-- First Column -->
        <div class="column is-flex is-flex-direction-row">
            <img src="../assets/photos/supplynationcertified.png" alt="Company Logo" class="supplynation mx-5"/>
            <p class="is-size-6 mt-4">
              Southstruct WA pty ltd is a supply nation registered business,
              we are a majority owned indigenous construction company.
            </p>
    
        </div>

        <!-- Second Column -->
        <div class="column has-text-left ml-5">
              <p class="mt-5 ml-5">0432 294 704</p>
              <p class="ml-5">drew.southstructwa@gmail.com</p>
        </div>

      </div>
      <p class="has-text-centered mt-5">&copy; {{ currentYear }} Southstruct WA. All rights reserved.</p>
 </div>

    </section>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const currentYear = ref(new Date().getFullYear());
</script>

<style scoped>
/* You can remove the custom styling for columns and rows */
</style>
