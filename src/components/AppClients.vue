<script>
export default {
    data() {
        return {
            clients: [
                {
                    image: 'testimonials-1',
                    text: 'Beauty is when you can appreciate yourself. When you love yourself, that’s when you’re most beautiful.',
                    name: 'Shelia McCourtney',
                    profession: 'architect'
                },
                {
                    image: 'testimonials-2',
                    text: 'Ability proceeds from a fusion of skills, knowledge, understanding and imagination, consolidated by ecperience.',
                    name: 'Luis Desalvo',
                    profession: 'creo tech'
                }
            ],
            activeItem: 0,
        };
    },
    methods: {
        nextSlide() {
            this.activeItem < this.clients.length - 1 ? this.activeItem++ : this.activeItem = 0;
            console.log(this.activeItem);
        },
        getImageUrl(name) {
            return new URL(`../assets/images/${name}.jpg`, import.meta.url).href
        }
    }
}
</script>

<template>
    <section class="clients">
        <div class="container text-center">
            <div class="row justify-content-center">
                <h3 class="mb-4">What Our  Clients Say</h3>
                <div class="col-7">
                    <div class="img-container my-4">
                        <img :src="getImageUrl(clients[activeItem].image)" :alt="clients[activeItem].name">
                    </div>
                    <i>{{ clients[activeItem].text }}</i>
                    <div class="my-4">
                        <strong>{{ clients[activeItem].name }}</strong>
                        <span class="text-uppercase">, {{ clients[activeItem].profession }}</span>
                    </div>
                    <div class="points-container d-flex justify-content-center">
                        <div v-for="i, index in 2" class="point me-2" :class="{'active': index == activeItem}" @click="nextSlide"></div>
                    </div>
                </div>
            </div>
            <div class="partner-logo-container d-flex justify-content-between align-items-center py-5 mt-5">
                <div class="img-container">
                    <img src="../assets/images/clients_partner_5-200x202.png" alt="">
                </div>
                <div class="img-container">
                    <img src="../assets/images/clients_partner_6-200x202.png" alt="">
                </div>
                <div class="img-container">
                    <img src="../assets/images/clients_partner_1-200x202.png" alt="">
                </div>
                <div class="img-container">
                    <img src="../assets/images/clients_partner_2-200x202.png" alt="">
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.clients {
    padding-top: 6.25rem;

    .row {
        .col-7 {
            .img-container {
                img {
                    border-radius: 100%;
                }
            }

            .points-container {
                .point {
                    width: .75rem;
                    height: .75rem;
                    border: 1px solid $brand-dark;
                    border-radius: 50%;
                    
                    &.active {
                        background-color: $brand-dark;
                    }
                }
            }
        }
    }
    
    .partner-logo-container {
        border-top: 1px solid lightgray;
        padding-right: 6.25rem;
        padding-left: 6.25rem;

        .img-container {
            max-width: 6.875rem;
        }
    }
}
</style>