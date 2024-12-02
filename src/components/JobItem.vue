<script setup lang="ts">
import { defineProps } from "vue"
import type { Job } from "@/types/job"

//default type of job
//const {
//  title = "Pet Care",
//  location = "One stop arcade",
//  salary = 1000,
//  id = "t001"
//} = defineProps<Job>() 

// Define props 
const props = 
  defineProps<{
    job: Job;
  }>()


</script>

<template>
    <div class="job-item">
        <h2 class="green">{{ props.job.title }}</h2>
        <p>Location: {{ props.job.location }}</p>
        <p>Salary: ${{ props.job.salary }}</p>
        <small>Job ID: {{ props.job.id }}</small>
    </div>

</template>

<style lang="css" scoped>
.job-item {
  border: 1px solid #ccc;
  padding: 1rem;
  margin-bottom: 1rem;
  border-radius: 8px;
}

</style>