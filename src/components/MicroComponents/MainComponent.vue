<template>
    <div class="col-2 g-3">
        <img :src="thumb" :alt="series">
        <div>
            <h5 class="text-white m-0">{{ series }}</h5>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'MainComponent',
        props: ['thumb', 'series'],
    }
</script>

<style lang="scss" scoped>
img {
    width: 200px;
    height: 200px;
}
</style>