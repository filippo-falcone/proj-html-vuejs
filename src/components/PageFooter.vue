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
    <footer>
        <div class="container d-flex flex-column align-items-center">
            <a href="#">
                    <img src="../assets/images/logo_seo_1x.png" alt="AvadaSEO logo">
                </a>
            <ul class="navbar-nav flex-row my-5 mb-lg-0">
                <li v-for="linkInfo, index in linksInfo" class="nav-item d-flex align-items-center me-4" @click="activeLink(index)">
                    <a class="nav-link" :class="{'active': index == activeItem}">{{ linkInfo.name }}</a>
                </li>
            </ul>
        </div>
    </footer>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

footer {
    padding-top: 3.125rem;
    padding-bottom: 3.125rem;
    
    .navbar-nav {
        .nav-link {
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