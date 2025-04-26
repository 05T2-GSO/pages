<template>
  <div class=".header">
    <Navbar />
    <div class="page-header">
      <h1>{{ title }}</h1>
      <h2>{{ secondaryTitle }}</h2>
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Navbar from '../components/Navbar.vue';

const title = ref("05T2 - GSO Website Transformation");
const secondaryTitle = ref("CS4850 - Senior Project, Spring 2025");
const description = ref("This project was in collaboration with the Georgia Symphony Orchestra (GSO)\
 to provide a Proof-of-Concept (POC) for a new website. The primary goal of the project was to identify and\
 propose solutions to the GSO's current website issues, with a strong focus on event systems and various potential SEO issues.\
 You can find the presentation and deliverables below or in the navbar above.");

</script>

<style scoped>
.header {
  display: contents;
}

.page-header {
  text-align: center;
  padding: 2rem 2rem;
  background-color: var(--background-light);
  max-width: 65vw;
  margin: 0 auto;
}

.page-header h1 {
  margin: 0;
  font-size: 2.5rem;
  color: var(--primary-color);
}

.page-header h2 {
  margin: 0.5rem 0;
  font-size: 1.5rem;
  color: var(--text-color);
}

.page-header p {
  margin-top: 0.5rem;
  font-size: 1.125rem;
  color: var(--text-color);
}
</style>
