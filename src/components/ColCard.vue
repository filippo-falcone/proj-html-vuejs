<script>
export default {
    props: {
        info: Object
    }
}
</script>

<template>
    <div class="col py-5 me-4">
        <i class="icon mb-4 fs-3" :class="info.icon"></i>
        <h4 class="mb-3">{{ info.title }}</h4>
        <p>{{ info.text }}</p>
        <a v-if="info.link" href="#">Read More ></a>
    </div>
</template>

<style scoped lang="scss"></style>