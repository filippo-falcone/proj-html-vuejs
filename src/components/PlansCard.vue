<script>
export default {
    props: {
        info: Object
    }
}
</script>

<template>
    <div class="col d-flex flex-column align-items-center py-5 me-4">
        <h4 class="mb-3">{{ info.title }}</h4>
        <div class="price-container d-flex align-items-center py-3">
            <div class="value">$</div>
            <div class="price fs-1">{{ info.price }}</div>
            <div>
                <div class="price cent text-start">{{ info.cent }}</div>
                <div class="month">monthly</div>
            </div>
        </div>
        <div class="pojects py-3">{{ info.project }} Projects</div>
        <div class="storage py-3">{{ info.storage }} GB Storage</div>
        <div class="usage py-3">{{ info.usage }} Users</div>
        <div class="btn-container py-3">
            <button v-if="!info.advised" class="btn big brand-outline-dark rounded-pill">start today</button>
            <button v-else class="btn big brand-primary rounded-pill">start today</button>
        </div>
    </div>
</template>

<style scoped lang="scss"></style>