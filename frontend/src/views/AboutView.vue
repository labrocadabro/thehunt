<script setup lang="ts">
import jobs from '../data/jobs.json'
</script>

<template>
  <div class="about">
    <ul>
      <li v-for="job in jobs" :key="job.id">
        <h2>{{ job.role }}</h2>
        <h3>{{ job.company }}</h3>
        <p><a :href="job.url" target="_blank">Apply</a></p>
        <p v-html="job.description"></p>
      </li>
    </ul>
  </div>
</template>
