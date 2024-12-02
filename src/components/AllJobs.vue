<script setup lang="ts">
import type { Job } from '@/types/job';
import JobItem from './JobItem.vue';



//sample job data
const jobs: Job[] = [
    {   
        title: "Dog Walker", 
        location: "City Park", 
        salary: 1200, 
        id: "j001" 
    },
    {   
        title: "Cat Sitter", 
        location: "Downtown", 
        salary: 1500, 
        id: "j002" 
    },
    {   
        title: "Pet Groomer", 
        location: "Main Street", 
        salary: 1300, 
        id: "j003" 
    }
]

</script>

<template>
    <div class="all-jobs">
        <h1 class="green"> Available Jobs </h1>
        <div class="job-list">
            <JobItem v-for="job in jobs" :key="job.id" :job="job"/>
        </div>

    </div>

</template>

<style lang="css" scoped>
.all-jobs {
  padding: 1rem;
}

.job-list {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

</style>