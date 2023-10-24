<script setup>
import TungaIcon from '../assets/TungaIcon.vue';


</script>

<template>
      <nav class="navbar navbar-expand-lg bg-body-tertiary fixed-top">
        <div class="container-fluid">
            <RouterLink class="navbar-brand" to="/"><TungaIcon width="50"/></RouterLink>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse justify-content-center" id="navbarSupportedContent">
            <ul class="navbar-nav">
                <li class="nav-item">
                    <RouterLink class="nav-link active" aria-current="page" to="/">Home</RouterLink>
                </li>
                <li class="nav-item">
                    <RouterLink class="nav-link active" aria-current="page" to="/projects">Projects</RouterLink>
                </li>
                <li class="nav-item">
                    <RouterLink class="nav-link active" aria-current="page" to="/funding">Funding</RouterLink>
                </li>
                <!-- <li class="nav-item">
                    <a class="nav-link" href="#">Link</a>
                </li> -->
                <!-- <li class="nav-item dropdown">
                <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                    Dropdown
                </a>
                <ul class="dropdown-menu">
                    <li><a class="dropdown-item" href="#">Action</a></li>
                    <li><a class="dropdown-item" href="#">Another action</a></li>
                    <li><hr class="dropdown-divider"></li>
                    <li><a class="dropdown-item" href="#">Something else here</a></li>
                </ul>
                </li> -->
                <!-- <li class="nav-item">
                <a class="nav-link disabled" aria-disabled="true">Disabled</a>
                </li> -->
            </ul>
            <form class="d-flex" role="search">
                <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
                <button class="btn btn-outline-purple" type="submit">Search</button>
            </form>
            </div>
        </div>
    </nav>
</template>

<style scoped>
 .btn-outline-purple{
    border-color: purple;
 }
</style>
