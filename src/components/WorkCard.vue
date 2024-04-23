<script>
export default {
    props: {
        info: Object
    },
    methods: {
        getImageUrl(name) {
            return new URL(`../assets/images/${name}.jpg`, import.meta.url).href
        }
    }
}
</script>

<template>
    <div class="col-4">
        <div class="img-container">
            <img :src="getImageUrl(info.image)" alt="">
            <div class="hover-container d-flex justify-content-center align-items-center">
                <i class="fa-solid fa-link fs-3"></i>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss"></style>