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
        <div class="work-card">
            <div class="card-img">
                <img :src="getImageUrl(info.image)" alt="">
            </div>
            <div class="card-text mt-4">
                <h4>{{ info.title }}</h4>
                <small>{{ info.date }}</small>
                <p class="mt-3">{{ info.text }}</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss"></style>