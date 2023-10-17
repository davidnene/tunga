<script setup>
import { Icon } from '@iconify/vue';
  defineProps({
    tunga: {
      type: String,
      required: true,
    },
  })
</script>

<template>
  <h1>Karibu {{ tunga }}!</h1>
  <Icon icon="svg-spinners:blocks-wave" color="purple" width="300" />
</template>
