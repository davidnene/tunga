<script setup>
    defineProps({
        author: {
            type: String,
            required: true,
        },
        role: {
            type: String,
            required: true,
        },
        link: {
            required: true,
        },
        title: {
            type: String,
            required: true,
        },
    })
</script>

<template>
    <div>
        <div class="text-center">
        <h4>{{ title }}</h4>
        <iframe width="600" height="450" :src = "link" style="border:0" allowfullscreen></iframe>
        <h6>Author: {{ author }}</h6>
        <h6>Role: {{ role }}</h6>
    </div>
    </div>
</template>

<style lang="scss" scoped>
.dash-outline {
    border-color: darkblue;
    border: 10px;
}
</style>