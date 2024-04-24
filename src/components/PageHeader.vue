<script>
import { callWithAsyncErrorHandling, onMounted } from 'vue';

export default {
    props: {
        linksInfo: Array,
        isActive: String
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
    <header :class="isActive">
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
                        <li v-for="linkInfo, index in linksInfo" class="nav-item d-flex align-items-center me-4" @click="activeLink(index)">
                            <a v-if="!linkInfo.button" class="nav-link" :class="{'active': index == activeItem}" :href="linkInfo.href">{{ linkInfo.name }}</a>
                            <button v-if="linkInfo.name === 'Careers'" class="btn small brand-outline-primary">apply</button>
                            <button v-if="linkInfo.button" class="btn big brand-primary rounded-pill">{{ linkInfo.name }}</button>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </header>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;
header {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 3;

    &.active {
        background-color: $brand-tertiary;
    }

    .navbar {
        .navbar-collapse {
            .nav-link {
                color: $brand-light-secondary;
                cursor: pointer;
    
                &.active {
                    color: $brand-primary;
                }
    
                &:hover {
                    color: $brand-primary;
                }
            }

            &.collapsing {
                .nav-item {
                    justify-content: flex-end;
                }
            }

            &.show {
                .nav-item {
                    justify-content: flex-end;
                }
            }
        }
    }
}
</style>