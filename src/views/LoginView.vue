<script setup>
import AuthIcon from '../assets/AuthIcon.vue';

</script>

<template>
    <div class="container cust-padding">
        <div class="row">
        <div class="col-md-4 padding-auto">

        </div>
        <div class="col-md-4 padding-auto">
        <form>
            <div class="row mb-3">
                <label for="inputEmail3" class="col-sm-2 col-form-label">Email</label>
                <div class="col-sm-10">
                <input type="email" class="form-control" id="inputEmail3" required>
                </div>
            </div>
            <div class="row mb-3">
                <label for="inputPassword3" class="col-sm-2 col-form-label" required>Password</label>
                <div class="col-sm-10">
                <input type="password" class="form-control" id="inputPassword3">
                </div>
            </div>
            <!-- <fieldset class="row mb-3">
                <legend class="col-form-label col-sm-2 pt-0">Radios</legend>
                <div class="col-sm-10">
                <div class="form-check">
                    <input class="form-check-input" type="radio" name="gridRadios" id="gridRadios1" value="option1" checked>
                    <label class="form-check-label" for="gridRadios1">
                    First radio
                    </label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" name="gridRadios" id="gridRadios2" value="option2">
                    <label class="form-check-label" for="gridRadios2">
                    Second radio
                    </label>
                </div>
                <div class="form-check disabled">
                    <input class="form-check-input" type="radio" name="gridRadios" id="gridRadios3" value="option3" disabled>
                    <label class="form-check-label" for="gridRadios3">
                    Third disabled radio
                    </label>
                </div>
                </div>
            </fieldset> -->
            <div class="row mb-3">
                <div class="col-sm-10 offset-sm-2">
                <div class="form-check">
                    <input class="form-check-input" type="checkbox" id="gridCheck1">
                    <label class="form-check-label" for="gridCheck1">
                    Remember Me
                    </label>
                </div>
                </div>
            </div>
            <div class="row">
                    <div class="col-md-4" style="color: white;">
                        <button type="submit" class="btn btn-bg-purple">Sign in</button>
                    </div>
                    <div class="col-md-4">
                        <p>Don't have an account?</p>
                    </div>
                    <div class="col-md-4">
                        <RouterLink class="btn btn-outline-purple" aria-current="page" to="/signup">Sign up</RouterLink>
                    </div>
                </div>
            </form>
        </div>
    </div>
    </div>
</template>

<style lang="scss" scoped>

</style>