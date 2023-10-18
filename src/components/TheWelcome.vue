<script setup>
import { Icon } from '@iconify/vue';
import { ref } from 'vue';
import TungaIcon from '../assets/TungaIcon.vue';
  defineProps({
    tunga: {
      type: String,
      required: true,
    },
  })

  const play = ref(true);
</script>

<template>
  <div class="container px-4 text-center">
  <div class="row gx-2">
    <div class="col-sm-12 col-md-6">
     <div class="p-3">
      <h1>Karibu {{ tunga }}!</h1>
      <p class="">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Lectus proin nibh nisl condimentum. Tincidunt ornare massa eget egestas purus viverra. Vitae congue eu consequat ac felis donec et odio. Cras ornare arcu dui vivamus arcu felis. Non sodales neque sodales ut etiam sit amet nisl purus. Ornare suspendisse sed nisi lacus sed viverra tellus in. Turpis egestas integer eget aliquet nibh praesent tristique. Cursus mattis molestie a iaculis at erat. Mi quis hendrerit dolor magna eget est lorem ipsum. Facilisi nullam vehicula ipsum a arcu. Porttitor rhoncus dolor purus non. Aenean pharetra magna ac placerat vestibulum.
      </p>
     </div>
    </div>
    <!-- <div class="col">
      <div class="p-3">
        <Icon icon="svg-spinners:bars-scale-middle" color="purple" width="100"/>
      </div>
    </div> -->
    <div class="col-sm-12 col-md-6">
      <div class="p-3">
        <a @click="play = !play" v-if="play">
          <TungaIcon/>
        </a>
        <a @click="play = !play" v-else="play">
          <Icon icon="svg-spinners:bars-scale-middle" color="purple" width="300"/>
        </a>
      </div>
    </div>
  </div>
</div>
</template>
