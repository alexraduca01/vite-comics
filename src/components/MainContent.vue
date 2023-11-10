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
                <button class="bg-primary py-3 px-5 text-white text-uppercase fs-5" @click="loadMore()">
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
                randomTitles: ['Laughing Dream', 'The Dying Predator', 'Something of Light', "The Theft's Moons", 'The Hunter of the Rings', 'Lords in the Courage', 'Hard Dreamer', 'The Burning Death', 'Voyager of Husband', "The Serpents's Teacher", 'The Academy of the Boyfriend', 'Dreams in the Waves'],
            }
        },
        methods: {
            loadMore(){
                for(let i = 0; i < 12; i++){
                    this.dcComics.push({
                        thumb: 'https://source.unsplash.com/random?',
                        series: this.randomTitles[this.getRndInteger(0, this.randomTitles.length - 1)],
                    })
                }
            },
            getRndInteger(min, max) {
                return Math.floor(Math.random() * (max - min + 1) ) + min;
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