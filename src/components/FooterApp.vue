<template>
    <footer>
        <div class="container d-flex p-0 align-items-center position-relative py-5">
            <div class="col-4 d-flex gap-4">
                <div>
                    <ul class="m-0">
                        <li class="text-uppercase mb-2"><h5 class="text-white">dc comics</h5></li>
                        <li v-for="item in dcComics" class="my-font-size">{{ item }}</li>
                    </ul>
                    <ul class="m-0 mt-5">
                        <li class="text-uppercase mb-2"><h5 class="text-white">shop</h5></li>
                        <li v-for="item in shop" class="my-font-size">{{ item }}</li>
                    </ul>
                </div>
                <div>
                    <ul class="m-0"> 
                        <li class="text-uppercase mb-2"><h5 class="text-white">dc</h5></li>
                        <li v-for="item in dc" class="my-font-size">{{ item }}</li>
                    </ul>
                </div>
                <div>
                    <ul class="m-0">
                        <li class="text-uppercase mb-2"><h5 class="text-white">sites</h5></li>
                        <li v-for="item in sites" class="my-font-size">{{ item }}</li>
                    </ul>
                </div>
            </div>
            <div class="col-8 d-flex justify-content-end ">
                <img src="img/dc-logo-bg.png" alt="big-logo">
            </div>
        </div>
    </footer>
</template>

<script>
    export default {
        name: 'FooterApp',
        data(){
            return {
                dcComics: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News'],
                shop: ['Shop DC', 'Shop DC Collectibles'],
                dc: ['Terms Of Use', 'Privacy Policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us'],
                sites: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa'],
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/css/main.scss' as *;

footer {
    background-image: url(img/footer-bg.jpg);
    background-size: 100%;
    background-repeat: no-repeat;
}
img {
    position: absolute;
    top: -25%;
    right: 0;
    width: 50%;
}
li {
    list-style: none;
    color: $main-text-color;
}
h5 {
    margin: 0;
}
.my-font-size {
    font-size: 0.9rem;
}
</style>