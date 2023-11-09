<template>
    <nav>
        <div class="container d-flex justify-content-around">
            <div v-for="element in divContent" class="d-flex align-items-center py-5 cursor-pointer">
                <div>
                    <img :src="element.image" :alt="element.title">
                </div>
                <span class="ms-3 text-white">{{ element.title }}</span>
            </div>
        </div>
    </nav>
</template>

<script>
    export default {
        name: 'NavbarComponent',
        data(){
            return {
                divContent: [
                    {
                        title: 'digital comics',
                        image: 'img/buy-comics-digital-comics.png',
                    },
                    {
                        title: 'dc merchandise',
                        image: 'img/buy-comics-merchandise.png',
                    },
                    {
                        title: 'subscription',
                        image: 'img/buy-comics-subscriptions.png',
                    },
                    {
                        title: 'comic shop locator',
                        image: 'img/buy-comics-shop-locator.png',
                    },
                    {
                        title: 'dc power visa',
                        image: 'img/buy-dc-power-visa.svg',
                    },
                ],
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/css/main.scss' as *;
nav {
    margin: 0;
    background-color: $main-color;
}
img {
    width: 55px;
    height: 65px;
}
.cursor-pointer {
    cursor: pointer;
}
</style>