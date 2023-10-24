<script setup>
    import { Icon } from '@iconify/vue';
    defineProps({
        name: {
            type: String,
            required: true,
        },
        img: {
            required: true
        },
    })
</script>

<template>
    <div>
        <div class="card body-padding" style="width: 18rem;">
            <Icon :icon= "img.icon" :style="{color: img.style.color}" :width="img.width"/>
            <div class="card-body ">
                <h4>{{ name }}</h4>
                <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                <a href="#">Learn more..</a>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .body-padding{
        height: 250px;
    }
</style>