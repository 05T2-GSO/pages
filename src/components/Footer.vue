<template>
  <footer class="page-footer">
    <p>&copy; {{ new Date().getFullYear() }} GSO, KSU, & Team Members </p>
  </footer>
</template>

<script setup></script>

<style scoped>
.page-footer {
  text-align: center;
  padding: 2rem 0;
  background-color: var(--background-light);
  border-top: 1px solid #eee;
}

.page-footer p {
  margin: 0;
  color: var(--text-color);
  font-size: 0.9rem;
}
</style>
