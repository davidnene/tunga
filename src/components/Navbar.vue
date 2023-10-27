<script setup>
import { Icon } from '@iconify/vue';
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

            <RouterLink class="btn-pos-signup" aria-current="page" to="/login" title="sign up"><Icon icon="bi:person-lock" color="darkblue" width="40" /></RouterLink>
            <!-- <RouterLink class="btn btn-outline-purple btn-pos-login" aria-current="page" to="/login">Login</RouterLink> -->
            </div>
        </div>
    </nav>
</template>

<style scoped>
 .btn-bg-purple{
    background-color: purple;
    color: white;
 }
 .btn-pos-signup {
    position: relative;
    left: 40%;
 }


 .btn-pos-login {
    position: relative;
    left: 30.5%;
    color: purple;
 }
</style>
