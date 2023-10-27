<script setup>
import Quote from '../components/Quote.vue';
import TheWelcome from '../components/TheWelcome.vue'
import ImageCard from '../assets/ImageCard.vue'
import NavDrawer from '../components/NavDrawer.vue';



const data = [
  {
    "projectName": "LLMs in Health Care",
    "projectImage": {
      "icon": "ic:baseline-corporate-fare",
      "style": {
        "color": "darkblue",
      },
      "width": "150",
    },
    "projectLink" : ""
  },

  {
    "projectName": "LLMs in Agriculture",
    "projectImage": {
      "icon": "ic:baseline-spa",
      "style": {
        "color": "darkblue",
      },
      "width": "150",
    },
    "projectLink" : ""
  },
  {
    "projectName": "ASR in Linguistics",
    "projectImage": {
      "icon": "ic:baseline-forum",
      "style": {
        "color": "darkblue",
      },
      "width": "150",
    },
    "projectLink" : ""
  },
  
  {
    "projectName": "ML in Security",
    "projectImage": {
      "icon": "ic:baseline-gpp-good",
      "style": {
        "color": "darkblue",
      },
      "width": "150",
    },
    "projectLink" : ""
  },
  {
    "projectName": "ML in Finance",
    "projectImage": {
      "icon": "ic:baseline-euro",
      "style": {
        "color": "darkblue",
      },
      "width": "150",
    },
    "projectLink" : ""
  },
]
</script>

<template>
  <main class="cust-padding">
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
    <!-- <NavDrawer/> -->
  </main>
</template>
