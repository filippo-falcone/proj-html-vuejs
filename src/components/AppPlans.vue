<script>
import PlansCard from './PlansCard.vue';

export default {
    components: {
        PlansCard
    },
    data() {
        return {
            info: [
                {
                    title: 'Standard',
                    price: 19,
                    cent: 99,
                    project: 5,
                    storage: 5,
                    usage: 'Unlimited',
                    advised: false
                },
                {
                    title: 'Premium',
                    price: 29,
                    cent: 99,
                    project: 10,
                    storage: 15,
                    usage: 'Unlimited',
                    advised: false
                },
                {
                    title: 'Professional',
                    price: 39,
                    cent: 99,
                    project: 15,
                    storage: 30,
                    usage: 'Unlimited',
                    advised: true
                },
                {
                    title: 'Extreme',
                    price: 59,
                    cent: 99,
                    project: 'Unlimited',
                    storage: 'Unlimited',
                    usage: 'Unlimited',
                    advised: false
                }
            ]
        };
    }
}
</script>

<template>
    <section id="plans">
        <div class="container text-center">
            <div class="row">
                <div class="col-12 d-flex justify-content-center">
                    <div class="text">
                        <h3 class="mb-4">Our Plans</h3>
                        <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.</p>
                    </div>
                </div>
                <PlansCard v-for="singleInfo in info" :info="singleInfo"></PlansCard>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
@use '../style/partials/variables' as *;

#plans {
    padding-top: 6.25rem;
    padding-bottom: 6.25rem;
    background-image: url(../assets/images/background1.jpg);
    
    .row {
        .col-12 {
            .text {
                color: $brand-light-tertiary;
                width: 40%;

                p {
                    color: $brand-light-tertiary;
                }
            }
        }

        .col {
            background-color: $brand-light-tertiary;

            div {
                color: $brand-dark-light;
            }

            .price-container {
                .value {
                    padding-top: .8125rem ;
                    font-size: .875rem;
                    align-self: flex-start;
                }

                .price {
                    color: $brand-secondary;

                    &.cent {
                         font-size: .875rem;
                    }
                }

                .month {
                    font-size: .625rem;
                }
            }

            &:hover {
                h4 {
                    color: $brand-secondary;
                }
            }
        }
    }
}
</style>