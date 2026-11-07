<template>
<h2>Spontane Treffen in Berlin!</h2>

<ul>
  <li v-for="meetup in meetups" :key="meetup.title">
    {{ meetup.title }} - {{ meetup.location }}
    </li>
</ul>
</template>

<script setup lang="ts">
const meetups = [
{
  title: "Kaffee trinken",
  location: "Berlin-Mitte",
  category: "Freizeit",
  date: "2026-11-10",
  time: "15:00",
  maxParticipants: 5
},
{
  title: "Spazieren gehen",
  location: "Trepotwer Park",
  category: "Outdoor",
  date: "2026-11-11",
  time: "14:00",
  maxParticipants: 8
},
{
  title: "Gemeinsam lernen",
  location: "Treskowalle HTW Berlin",
  category: "Lernen",
  date: "2026-11-12",
  time: "12:00",
  maxParticipants: 4
},
]
</script>

<style scoped>
</style>
