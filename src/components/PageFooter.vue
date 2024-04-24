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
            <a class="mt-4 mb-5" href="#">
                    <img src="../assets/images/logo_seo_1x.png" alt="AvadaSEO logo">
                </a>
            <ul class="navbar-nav flex-row flex-wrap align-items-center mb-lg-0">
                <li v-for="linkInfo, index in linksInfo" class="nav-item d-flex align-items-center me-4" @click="activeLink(index)">
                    <a class="nav-link" :class="{'active': index == activeItem}" :href="linkInfo.href">{{ linkInfo.name }}</a>
                </li>
            </ul>
            <div class="copyright mt-5 mb-4">
                <small class="pe-2">© Copyright 2012-2024</small>
                <small class="px-2">Avada Theme by <a href="https://boolean.careers/" target="_blank">Boolean</a></small>
                <small class="px-2">All Rights Reserved</small>
                <small class="ps-2 pe-3">Powered by <a href="https://github.com/filippo-falcone" target="_blank">filippo-falcone</a></small>
            </div>
            <div class="social d-flex justify-content-between align-items-center">
                <div class="me-3">
                    <a href="#">
                        <i class="fa-brands fa-facebook-f"></i>
                    </a>
                </div>
                <div class="me-3">
                    <a href="#">
                        <i class="fa-brands fa-instagram"></i>
                    </a>
                </div>
                <div class="me-3">
                    <a href="#">
                        <i class="fa-brands fa-x-twitter"></i>
                    </a>
                </div>
                <div class="me-3">
                    <a href="#">
                        <i class="fa-brands fa-youtube"></i>
                    </a>
                </div>
            </div>
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

    .copyright {
        color: $brand-dark-light;

        small:not(:last-child) {
            border-right: .0625rem solid $brand-dark-light;
        }
        
        a {
            color: $brand-dark-light;
            font-weight: 700;
            text-decoration: none;

            &:hover {
                color: $brand-primary;
            }
        }
    }

    .social {
        a {
            color: $brand-dark-light;
            &:hover {
                color: $brand-primary;
            }
        }
    }
}
</style>