<template>
  <section class="deliverable-buttons">
    <h2>Deliverable Links</h2>
    <div class="button-container">
      <a :href="githubLink" target="_blank" class="cta-button">GitHub</a>
      <a :href="presentationLink" target="_blank" class="cta-button">Presentation</a>
      <a :href="reportLink" target="_blank" class="cta-button">Final Report</a>
      <a :href="sponsorRecLink" target="_blank" class="cta-button">Sponsor Guide</a>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';

defineProps({
  githubLink: {
    type: String,
    default: "#"
  },
  presentationLink: {
    type: String,
    default: "#"
  },
  reportLink: {
    type: String,
    default: "#"
  },
  sponsorRecLink: {
    type: String,
    default: "#"
  }
});
</script>

<style scoped>
.deliverable-buttons {
  text-align: center;
  padding: 2rem 0;
}

.button-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 2rem;
  margin-top: 2rem;
}

.cta-button {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  font-size: 1.125rem;
  font-weight: 600;
  color: var(--secondary-color, #fff);
  background-color: var(--primary-color);
  text-decoration: none;
  border: 2px solid transparent;
  border-radius: 0.5rem;
  transition: background-color 0.15s ease, color 0.15s ease, border-color 0.15s ease;
}

.cta-button:hover {
  background-color: var(--secondary-color);
  color: var(--primary-color);
  border-color: var(--primary-color);
}

.cta-button:active {
  transform: translateY(0);
}
</style>