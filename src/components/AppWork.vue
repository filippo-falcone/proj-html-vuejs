<script>
import WorkCard from './WorkCard.vue';

export default {
    components: {
        WorkCard
    },
    data() {
        return {
            info: [
                {
                    image: 'case-study-gallery-3-1'
                },
                {
                    image: 'case-study-gallery-2'
                },
                {
                    image: 'case-study-gallery-1-1'
                },
                {
                    image: 'case-study-gallery-4-1'
                },
                {
                    image: 'case-study-gallery-5-1'
                },
                {
                    image: 'case-study-gallery-6-1'
                }
            ]
        };
    }
}
</script>

<template>
    <section class="what-we-work">
        <div class="container text-center">
            <div class="row g-3">
                <div class="col-12 d-flex justify-content-center">
                    <div class="text">
                        <h3 class="mb-4">Our Work</h3>
                        <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.</p>
                    </div>
                </div>
                <WorkCard v-for="singleInfo in info" :info="singleInfo"></WorkCard>
                <div class="col-12 btn-container py-4">
                    <button class="btn big brand-primary rounded-pill me-3">view our work</button>
                </div>
           </div>
        </div>
    </section>
</template>

<style lang="scss">
@use '../style/partials/variables' as *;

.what-we-work {
    padding-top: 6.25rem;
    padding-bottom: 6.25rem;
    background-color: $brand-light-secondary;

    .row {
        .col-12 {
            .text {
                width: 40%;
            }
        }

        .col-4 {
            .img-container {
                position: relative;

                &:hover {
                    .hover-container {
                        opacity: 1;
                    }
                }
            }

            .hover-container {
                background-image: linear-gradient(to bottom, $brand-secondary-light, $brand-light-secondary);
                color: $brand-light-primary;
                position: absolute;
                top: 0;
                right: 0;
                bottom: 0;
                left: 0;
                opacity: 0;
            }
        }
    }
}
</style>