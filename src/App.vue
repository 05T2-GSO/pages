<template>
  <div id="app">
    <Header :github-link="githubLink"
        :presentation-link="presentationLink"
        :report-link="reportLink"
        :sponsor-rec-link="sponsorRecLink"/>
    <div class="break"></div>
    <main class="content">
      <Links
        :github-link="githubLink"
        :presentation-link="presentationLink"
        :report-link="reportLink"
        :sponsor-rec-link="sponsorRecLink"/>
      <div class="break"></div>
      <section class="team">
        <h2>Team Members</h2>
        <div class="team-grid">
          <div class="member" v-for="member in team" :key="member.name">
            <img :src="member.photo" :alt="member.name" />
            <h3>{{ member.name }}</h3>
            <p>{{ member.role }}</p>
          </div>
        </div>

      </section>
    </main>
    <Footer/>
  </div>
</template>

<script setup>
import { ref } from 'vue';

import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Links from './components/Links.vue';

import noah_bio from './assets/bio_pics/noah_bio.webp';
import jonathan_bio from './assets/bio_pics/jonathan_bio.webp';
import kevin_bio from './assets/bio_pics/kevin_bio.webp';
import rashmi_bio from './assets/bio_pics/rashmi_bio.webp';

import reportLink from './assets/pdfs/final-report.pdf';
import sponsorRecLink from './assets/pdfs/sponsor-recommendations.pdf';
const githubLink = ref("https://github.com/05T2-GSO/");

// Change these links to the actual URLs of the deliverables
const presentationLink = ref("https://example.com/presentation");


import { reactive } from 'vue';

const team = reactive([
  { name: 'Noah Minch', role: 'Backend', photo: noah_bio },
  { name: 'Jonathan Turner', role: 'Frontend', photo: jonathan_bio },
  { name: 'Kevin Syhavong', role: 'Design', photo: kevin_bio },
  { name: 'Rashmi Wagde', role: 'QA', photo: rashmi_bio },
]);
</script>

<style>
:root {
  --primary-color: #EA6952;
  /* GSO Orange */
  --background-color: #fff;
  /* White */
  --background-light: #fff;
  /* Same as background color, decided not to have to backgrounds.  */
  --text-color: #333333;
  /* dark gray */
}

body,
#app {
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
  background: var(--background-color);
  color: var(--text-color);
  display: contents;
}

.content {
  padding: 0 2rem;
  min-height: 60vh;
}

.team {
  max-width: 960px;
  margin: 0 auto;
  text-align: center;
  padding-top: 2rem;
}

.team-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1.25fr));
  gap: 2.5rem;
  margin-top: 1.5rem;
}

.member img {
  border-radius: 25%;
  width: 200px;
  height: 200px;
  object-fit: cover;
}

.member h3 {
  margin: 0.5rem 0 0.25rem;
}

.member p {
  margin: 0;
  font-size: 0.9rem;
  color: #666;
}

.break::after {
  content: "";
  display: block;
  width: 50vw;                           
  height: 2px;                           
  background-color: var(--primary-color, #e94e77);
  opacity: 0.4;                          
  margin: 0.5rem auto 0;                 
}
</style>
