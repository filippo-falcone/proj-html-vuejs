<script>
import ColCard from './ColCard.vue';

export default {
    components: {
        ColCard
    },
    data() {
        return {
            info: [
                {
                    icon: 'fa-brands fa-google',
                    title: 'Google SEO',
                    text: 'Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.',
                    link: true
                },
                {
                    icon: 'fa-solid fa-gear',
                    title: 'Brand Strategy',
                    text: 'Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.',
                    link: true
                },
                {
                    icon: 'fa-solid fa-building',
                    title: 'Local SEO',
                    text: 'Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.',
                    link: true
                },
                {
                    icon: 'fa-solid fa-chart-column',
                    title: 'SEO Analysis',
                    text: 'Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.',
                    link: true
                }
            ]
        };
    }
}
</script>

<template>
    <section id="what-we-do">
        <div class="container text-center pt-5">
            <div class="row">
                <div class="col-12 d-flex justify-content-center">
                    <div class="text">
                        <h3 class="mb-4">See Our Top Notch Services</h3>
                        <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.</p>
                    </div>
                </div>
                <ColCard v-for="singleInfo in info" :info="singleInfo"></ColCard>
           </div>
        </div>
    </section>
</template>

<style lang="scss">
@use '../style/partials/variables' as *;

#what-we-do {
    padding-top: 2rem;
    padding-bottom: 6.25rem;
    background-color: $brand-tertiary;
    background-image: url(../assets/images/pattern_background.png);
    background-position: center;
    background-size: contain;
    background-repeat: no-repeat;
    color: $brand-light-primary;
    
    p {
        color: $brand-light-primary;
    }

    .row {
        .col-12 {

            .text {
                width: 40%;
            }
        }

        .col {
            background-color: $brand-tertiary-light;

            &:hover {
                h4 {
                    color: $brand-primary;
                }
            }

            .icon {
                color: $brand-primary;
            }
            
            p {
                padding-left: 2rem;
                padding-right: 2rem;
            }

            a {
                color: $brand-primary;
                text-decoration: none;

                &:hover {
                    text-decoration: underline;
                }
            }
        }
    }
}
</style>