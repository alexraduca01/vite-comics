<template>
    <div class="my-container py-5">
        <div class="container d-flex justify-content-between">
            <div class="d-flex align-items-center ">
                <div class="sign-up p-3 fs-5 text-uppercase ">sign up now!</div>
            </div>
            <div class="d-flex justify-content-between align-items-center gap-3">
                <span class="fs-5 text-uppercase ">follow us</span>
                <img src="img/footer-facebook.png" alt="facebook">
                <img src="img/footer-twitter.png" alt="twitter">
                <img src="img/footer-youtube.png" alt="youtube">
                <img src="img/footer-pinterest.png" alt="pinterest">
                <img src="img/footer-periscope.png" alt="periscope">
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'SecondFooter',
        data(){
            return {

            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/css/main.scss' as *;

.my-container {
    background-color: $main-background-color;
    position: relative;
    z-index: 1000;
}
.sign-up {
    color: white;
    border: 2px solid $main-color;
    cursor: pointer;
}
span {
    color: $main-color;
    cursor: pointer;
}
img {
    cursor: pointer;
}
</style>