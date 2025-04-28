<template>
    <nav class="navbar">
        <div class="nav-content">
            <div class="nav-title">
                <a href="/" class="home-title">{{ title }}</a>
            </div>
            <ul class="nav-list">
                <li>
                    <a target="_blank" :href="githubLink">GitHub</a>
                </li>
                <li>
                    <a :href="documentationLink">Documentation</a>
                </li>
                <li>
                    <a :href="presentationLink">Presentation</a>
                </li>
            </ul>
        </div>
    </nav>
</template>

<script setup>

import { ref } from 'vue';
const title = ref("GSO Website Transformation");
const githubLink = ref("https://github.com/05T2-GSO/");

// Change these links to the actual URLs of the deliverables
const documentationLink = ref("https://example.com/documentation");
const presentationLink = ref("https://example.com/presentation");
</script>

<style scoped>
.home-title {
    font-size: 2rem;
    font-weight: bold;
    color: #f1f1f1;
    text-decoration: none;
}

.nav-content {
    width: 75vw;
    justify-self: center;
    display: flex;
    justify-content: space-between;
}

.navbar {
    background-color: var(--primary-color);
    padding: 1rem 2rem;
    width: 100vw;
    display: grid;
}

.nav-list {
    justify-self: end;
    justify-content: end;
    list-style: none;
    display: flex;
    gap: 1.5rem;
    margin: 0;
    padding: 0;
}

.nav-list a, .nav-title a {
    color: white;
    text-decoration: none;
    font-weight: bold;
    font-size: large;
}

.nav-list a {
  position: relative;          
  display: inline-block;       
  text-decoration: none;
}

.nav-list a:hover {
  color: #fff;
  background-color: var(--primary-color);
}

.nav-list a::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: -2px;                
  width: 100%;
  height: 2px;                 
  background-color: #fff;  
  transform: scaleX(0);        
  transform-origin: center;    
  transition: transform 0.3s ease;
}

.nav-list a:hover::after {
  transform: scaleX(1);        
}
</style>
