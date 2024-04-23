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
                    icon: 'fa-solid fa-road',
                    title: 'Establish Goals',
                    text: 'Aliquam non elit lacus. Praesent aliquet, ipsum id scelerisque convallis, mi ligula euismond odio, vel dictum mi risus a mi.',
                    link: false
                },
                {
                    icon: 'fa-solid fa-video',
                    title: 'Work With a Team',
                    text: 'Cras semper auctor aliquam. Sed porta sed lacus sit amet consectetur. Lorem ipsum dolor sit amet, consectetur adipiscin.',
                    link: false
                },
                {
                    icon: 'fa-solid fa-droplet',
                    title: 'Get Results',
                    text: 'Vestibulum scelerisque egestas lectus sit amet molestie. Donec consectetur cursus est sed blandit. Nunc sed risus lacus.',
                    link: false
                }
            ]
        };
    }
}
</script>

<template>
    <section class="who-we-are">
        <div class="container text-center pt-5">
            <div class="row g-5">
                <div class="col-12 d-flex justify-content-center">
                    <div class="text">
                        <h3 class="mb-4">Meet The New Agency SEO Template From The Avada Team</h3>
                        <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.</p>
                    </div>
                </div>
                <ColCard v-for="singleInfo in info" :info="singleInfo"></ColCard>
           </div>
           <div>
                <img src="../assets/images/agency-seo-desk-front.jpg" alt="">
           </div>
        </div>
    </section>
</template>

<style lang="scss">
@use '../style/partials/variables' as *;

.who-we-are {
    background-color: $brand-light-primary;
    
    .row {
        .col-12 {
            .text {
                width: 40%;
            }
        }
        
        .col {
            background-color: $brand-light-tertiary;

            &:hover {
                h4 {
                    color: $brand-primary;
                }
            }

            .icon {
                color: $brand-primary;
            }
        }
    }
}
</style>