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
import { onMounted, ref } from 'vue'

onMounted(async () => {

const response = await fetch('https://spontyberlin-backend.onrender.com/meetup')
const data = await response.json()
meetups.value = [data]

})

const meetups = ref<Meetup[]>([])

interface Meetup {
title: string,
location: string
category: string
date: string
time: string
maxParticipants: number
}



</script>

<style scoped>
</style>
