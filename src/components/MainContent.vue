<template>
    <main>
        <section class="w-100 top-section position-relative">
            <h3 class="bg-primary text-white text-uppercase p-3">
                current series
            </h3>
        </section>
        <section class="w-100 bg-black p-5">
            <div class="container">
                <div class="row">
                    <MainComponent v-for="el in dcComics" :thumb="el.thumb" :series="el.series"/>
                </div>
            </div>
            <div class="d-flex justify-content-center mt-5">
                <button class="bg-primary py-3 px-5 text-white text-uppercase fs-5">
                    load more
                </button> 
            </div>
            
        </section>
    </main>
</template>

<script>
import axios from 'axios';
import MainComponent from './MicroComponents/MainComponent.vue';
    export default {
        name: 'MainContent',
        components: {
            MainComponent,
        },
        data(){
            return {
                dcComics: [],
            }
        },
        mounted(){
            axios.get('dc-comics.json').then(elements => {
                this.dcComics = elements.data;
            });
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/css/main.scss' as *;
.top-section {
    height: 40vh;
    background-image: url(img/jumbotron.jpg);
    background-size: 100%;
}
h3 {
    position: absolute;
    bottom: -8%;
    left: 22%;
    z-index: 2000;
}
</style>