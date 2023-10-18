<script setup>
import Quote from '../components/Quote.vue';
import TheWelcome from '../components/TheWelcome.vue'
import ImageCard from '../assets/ImageCard.vue'



const data = [
  {
    "projectName": "LLMs in Health Care",
    "projectImage": 'data:image/svg+xml,%3Csvg xmlns="http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg" width="80" height="80" viewBox="0 0 24 24"%3E%3Cpath fill="darkblue" d="M12 7V3H2v18h20V7H12zm-2 12H4v-2h6v2zm0-4H4v-2h6v2zm0-4H4V9h6v2zm0-4H4V5h6v2zm10 12h-8V9h8v10zm-2-8h-4v2h4v-2zm0 4h-4v2h4v-2z"%2F%3E%3C%2Fsvg%3E',
    "projectLink" : ""
  },

  {
    "projectName": "LLMs in Agriculture",
    "projectImage": "",
    "projectLink" : ""
  },
  {
    "projectName": "ASR in Linguistics",
    "projectImage": "",
    "projectLink" : ""
  },
]
</script>

<template>
  <main>
    <TheWelcome tunga="Tunga" />
    <Quote/>
    <div class="container overflow-hidden text-center">
        <div  class="row gx-1">
          <div v-for="project in data" class="col-sm-12 col-md-6 col-lg-4">
          <div  class="p-3">
          <ImageCard :name= project.projectName :img= project.projectImage />
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
