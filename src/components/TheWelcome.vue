<script setup>
  defineProps({
    tunga: {
      type: String,
      required: true,
    },
  })
</script>

<template>
  <h1>Karibu {{ tunga }}!</h1>
</template>
