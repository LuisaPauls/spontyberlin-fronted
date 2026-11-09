<script setup lang="ts">
import MeetupList from './components/MeetupList.vue'
import logo from './assets/logo.png'
</script>


<template>
<header>
<img :src="logo" alt="SpontyBerlin Logo" />
</header>

<main>
  <MeetupList />
</main>
</template>
