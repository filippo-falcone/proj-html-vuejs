<script>
export default {
    props: {
        linksInfo: Array
    },
    data() {
        return {
            activeItem: 0
        }
    },
    methods: {
        activeLink(index){
            this.activeItem = index;
        }
    }
}
</script>

<template>
    <header>
        <nav class="navbar navbar-expand-lg">
    <div class="container">
        <a class="navbar-brand" href="#">
            <img src="../assets/images/logo_seo_w_1x.png" alt="AvadaSEO logo">
        </a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse flex-grow-0" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                <li v-for="linkInfo, index in linksInfo" class="nav-item d-flex align-items-center" @click="activeLink(index)">
                    <a class="nav-link" :class="{'active': index == activeItem}">{{ linkInfo.name }}</a>
                    <button v-if="linkInfo.name === 'Careers'" class="btn btn-outline-primary">apply</button>
                </li>
                <button class="btn btn-success rounded-pill">get in touch now</button>
            </ul>
        </div>
    </div>
</nav>
    </header>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;
header {
    background-color: red;

    .navbar {
        .nav-link {
            color: $brand-light;
            cursor: pointer;

            &.active {
                color: $brand-primary;
            }

            &:hover {
                color: $brand-primary;
            }
        }
    }
}
</style>