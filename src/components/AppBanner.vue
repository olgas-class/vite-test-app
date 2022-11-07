<script>
export default {
    data() {
        return {
            imgName: `milano.jpg`
        }
    },
    methods: {
        getImagePath() {
            return new URL(`../assets/img/${this.imgName}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="banner">
        <img :src="getImagePath()" alt="">
    </div>
</template>

<style scoped>
.banner {
    width: 100%;
    height: 30vh;
}

.banner img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>