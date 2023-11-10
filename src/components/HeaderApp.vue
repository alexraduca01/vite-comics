<template>
    <header>
        <div class="container d-flex justify-content-between align-items-center p-3">
            <div>
                <img src="img/dc-logo.png" alt="logo">
            </div>
            <nav>
                <ul class="nav">
                    <li class="nav-item" @click="changeActiveIndex(content.id)" v-for="(content, index) in headerNavbar">
                        <a class="nav-link text-black text-uppercase" :class="activeElement(content.id)" href="#">{{ content.title }}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
    export default {
        name: 'HeaderApp',
        data(){
            return {
                headerNavbar: [
                    {
                        id: 1,
                        title: 'characters',
                    },
                    {
                        id: 2,
                        title: 'comics',
                    },
                    {
                        id: 3,
                        title: 'movies',
                    },
                    {
                        id: 4,
                        title: 'tv',
                    },
                    {
                        id: 5,
                        title: 'games',
                    },
                    {
                        id: 6,
                        title: 'collectibles',
                    },
                    {
                        id: 7,
                        title: 'videos',
                    },
                    {
                        id: 8,
                        title: 'fans',
                    },
                    {
                        id: 9,
                        title: 'news',
                    },
                    {
                        id: 10,
                        title: 'shop',
                    },  
                ],
                activeIndex: 1,
            }
        },
        methods: {
            changeActiveIndex(id){
                for(let i = 0; i < this.headerNavbar.length - 1; i++){
                    if(this.headerNavbar[i].id === id){
                        this.activeIndex = i;
                    };
                };
            },
            activeElement(id){
                if(this.headerNavbar[this.activeIndex].id === id){
                    return "is-active";
                };
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/css/main.scss' as *;
.is-active {
    color: $main-color!important;
    border-bottom: 5px solid $main-color;
}
</style>