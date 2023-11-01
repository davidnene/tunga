<script setup>
import Dash from '../components/Dash.vue';
import axios from 'axios';

const dashData = [
  {
  'author': 'David Nene',
  'role': 'Software Engineer',
  'title': 'Unemployment of Blue Collar Workers in the United States',
  'link': "https://lookerstudio.google.com/embed/reporting/bd962a96-6fab-4a52-924c-42c8bcf2187a/page/bGPgD",
  },
  {
  'author': 'Derrick Lubanga',
  'role': 'Data Scientist',
  'title': 'Climate Analysis Report',
  'link': "https://lookerstudio.google.com/embed/reporting/a75aefe9-7d81-4fa1-bbfd-5b93bf1b3e6d/page/p_shlc2t65ad"
  },
  {
  'author': 'Sharon Tonui',
  'role': 'Machine Learning Engineer',
  'title': 'Financial Analysis',
  'link': "https://lookerstudio.google.com/embed/reporting/2662dfc8-b4f4-4e38-b00d-54ca5d0f5627/page/yiRgD"
  },
  {
  'author': 'Linda Kelida',
  'role': 'Machine Learning Engineer',
  'title': 'Health Insurance Report',
  'link': "https://lookerstudio.google.com/embed/reporting/570ef279-416b-4f6c-bac7-d07e086e64b0/page/OSQgD"
  },
  {
  'author': 'Monilade Oladiran',
  'role': 'Business Analyst',
  'title': 'Adult Income Classification Report',
  'link': "https://lookerstudio.google.com/embed/reporting/2485ba8a-4454-4073-8314-23748c7661b2/page/2SggD",
  },
]

const token = localStorage.getItem("token");
// axios.config.defaults.header["Authorization"] = "Bearer "+token;
// await axios.post("http://")

</script>

<template>
  <main class="cust-padding">
        <div>
            <div class="container">
              <div class="row gy-4">
                <div v-for="dash in dashData" class="col-md-6">
                  <Dash :author = dash.author :role = dash.role :link = dash.link :title = dash.title />
                </div>
              </div>
            </div>
        </div>
    </main>
</template>

<style scoped>
</style>
