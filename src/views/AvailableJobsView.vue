<script setup lang="ts">
import AllJobs from '@/components/AllJobs.vue';




</script>

<template>
  <div class="about">   
    <div class="jobs">
      <AllJobs />
    </div>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    align-items: left;
  }
}
</style>
