<script>
export default {}
</script>

<template>
    <section class="news">
        <div class="container text-center">
            <div class="row g-3">
                <div class="col-12 d-flex justify-content-center">
                    <div class="text">
                        <h3 class="mb-4">Our News</h3>
                        <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.</p>
                    </div>
                 </div>
                <div class="col-4">
                    <div class="work-card">
                        <div class="card-img">
                            <img src="../assets/images/related-service-2-700x441.jpg" alt="">
                        </div>
                        <div class="card-text mt-4">
                            <h4>Why You Need A SEO Agency Now</h4>
                            <small>November 1st, 2017</small>
                            <p class="mt-3">ALorem ipsum dolor sit amet, consectetur adipiscing elit. In et scelerisque sem. Nunc molestie neque augue, at gravida mi blandit</p>
                        </div>
                    </div>
                </div>
                <div class="col-4">
                    <div class="work-card">
                        <div class="card-img">
                            <img src="../assets/images/related-service-4-700x441.jpg" alt="">
                        </div>
                        <div class="card-text mt-4">
                            <h4>Why You Need A SEO Agency Now</h4>
                            <small>November 1st, 2017</small>
                            <p class="mt-3">ALorem ipsum dolor sit amet, consectetur adipiscing elit. In et scelerisque sem. Nunc molestie neque augue, at gravida mi blandit</p>
                        </div>
                    </div>
                </div>
                <div class="col-4">
                    <div class="work-card">
                        <div class="card-img">
                            <img src="../assets/images/blog-post-6-700x441.jpg" alt="">
                        </div>
                        <div class="card-text mt-4">
                            <h4>Why You Need A SEO Agency Now</h4>
                            <small>November 1st, 2017</small>
                            <p class="mt-3">ALorem ipsum dolor sit amet, consectetur adipiscing elit. In et scelerisque sem. Nunc molestie neque augue, at gravida mi blandit</p>
                        </div>
                    </div>
                </div>
                <div class="col-12 btn-container py-4">
                    <button class="btn big brand-primary rounded-pill me-3">go to news</button>
                </div>
           </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.news {
    background-color: $brand-light-secondary;
    padding-top: 6.25rem;
    padding-bottom: 6.25rem;
    
    .row {
        .col-12 {
            .text {
                width: 40%;
            }
        }

        .col-4 {
            .work-card {
                .card-text {
                    h4 {
                        color: $brand-primary;
                    }

                    small {
                        color: $brand-dark-light;
                    }
                }
            }
        }
    }
}
</style>