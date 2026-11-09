<template>
<section class="meetup-list">
<h1>Spontane Treffen in Berlin!</h1>
<br>

<article v-for="meetup in meetups" :key="meetup.title" class="meetup-card">

   <h3> {{ meetup.title }} ({{ meetup.category }})</h3>
   <p> Treffpunkt: {{ meetup.location }} , am {{ meetup.date }} um {{ meetup.time }} Uhr</p>
   <p> Maximale Teilnehmer: {{ meetup.maxParticipants }}</p>

</article>
</section>
</template>

<script setup lang="ts">
const meetups = [
{
  title: "Kaffee trinken",
  location: "Berlin-Mitte",
  category: "Freizeit",
  date: "10/11/2026",
  time: "15:00",
  maxParticipants: 5
},
{
  title: "Spazieren gehen",
  location: "Trepotwer Park",
  category: "Outdoor",
  date: "11/11/2026",
  time: "14:00",
  maxParticipants: 8
},
{
  title: "Gemeinsam lernen",
  location: "Treskowalle HTW Berlin",
  category: "Lernen",
  date: "12/11/2026",
  time: "12:00",
  maxParticipants: 4
},
]
</script>

<style scoped>
</style>
