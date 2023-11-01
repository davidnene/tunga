<script setup>
import AuthIcon from '../assets/AuthIcon.vue';
import { ref, reactive } from 'vue';
import axios from 'axios';
import router from '../router/index';

const signUpData = reactive({
    name: "",
    email: "",
    password: "",
    password_confirmation: "",
});

const signUpError = ref('')

const sendSignup = async() => {
    try {
        const response = await axios.post("http://localhost:8000/api/register", {
            name: signUpData.name,
            email: signUpData.email,
            password: signUpData.password,
            password_confirmation: signUpData.password_confirmation
        });
        router.push('/login');
    } catch (error) {
        console.error("Error signing up: ",error)
        signUpError.value = error.response.data.errors;
    }
}

</script>

<template>
    <div class="container cust-padding">
        <div class="row">
        <div class="col-md-6 justify-content-center">
            <!-- <Icon icon="material-symbols:passkey" color="darkblue" width="300" /> -->
            <AuthIcon/>
        </div>
        <div class="col-md-6 justify-content-center">
        <form class="row g-3" @submit.prevent=sendSignup>
            <div class="col-12">
                <label for="inputName" class="form-label">Name</label>
                <input type="text" class="form-control" id="inputName" placeholder="Full name" v-model="signUpData.name">
            </div>
            <div class="col-md-12">
                <label for="inputEmail4" class="form-label">Email</label>
                <input type="email" class="form-control" id="inputEmail4" v-model="signUpData.email">
            </div>
                <p v-if="signUpError.email !== ''">{{ signUpError.email }}</p>
            <div class="col-md-6">
                <label for="inputPassword4" class="form-label">Password</label>
                <input type="password" class="form-control" id="inputPassword4" v-model="signUpData.password">
            </div>
            <div class="col-md-6">
                <label for="inputPassword4" class="form-label">Confirm Password</label>
                <input type="password" class="form-control" id="inputPasswordConfirm4" v-model="signUpData.password_confirmation">
            </div>
            <div>
                <p v-show="signUpError.password !== ''">{{ signUpError.password }}</p>
            </div>
            <!-- <div class="col-12">
                <label for="inputAddress" class="form-label">Address</label>
                <input type="text" class="form-control" id="inputAddress" placeholder="1234 Main St">
            </div>
            <div class="col-12">
                <label for="inputAddress2" class="form-label">Address 2</label>
                <input type="text" class="form-control" id="inputAddress2" placeholder="Apartment, studio, or floor">
            </div>
            <div class="col-md-6">
                <label for="inputCity" class="form-label">City</label>
                <input type="text" class="form-control" id="inputCity">
            </div>
            <div class="col-md-4">
                <label for="inputState" class="form-label">State</label>
                <select id="inputState" class="form-select">
                <option selected>Choose...</option>
                <option>...</option>
                </select>
            </div>
            <div class="col-md-2">
                <label for="inputZip" class="form-label">Zip</label>
                <input type="text" class="form-control" id="inputZip">
            </div>
            <div class="col-12">
                <div class="form-check">
                <input class="form-check-input" type="checkbox" id="gridCheck">
                <label class="form-check-label" for="gridCheck">
                    Check me out
                </label>
                </div>
            </div> -->
            <div>
                <div class="row">
                    <div class="col-md-4" style="color: white;">
                        <button type="submit" class="btn btn-bg-purple">Sign up</button>
                    </div>
                    <div class="col-md-4">
                        <p>Already have an account?</p>
                    </div>
                    <div class="col-md-4">
                        <RouterLink class="btn btn-outline-purple" aria-current="page" to="/login">Sign in</RouterLink>
                    </div>
                </div>
            </div>
    
        </form>
    </div>
    </div>
    </div>
</template>


<style lang="scss" scoped>

</style>