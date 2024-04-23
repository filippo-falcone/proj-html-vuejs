<script>
export default {}
</script>

<template>
    <section class="what-we-do">
        <div class="container text-center pt-5">
            <div class="row g-5">
                <div class="col-12 d-flex justify-content-center">
                    <div class="text">
                        <h3 class="mb-4">See Our Top Notch Services</h3>
                        <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.</p>
                    </div>
                 </div>
                 <div class="col py-5 me-4">
                    <i class="fa-solid fa-road mb-4 fs-3"></i>
                    <h4 class="mb-3">Google SEO</h4>
                    <p>Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.</p>
                    <a href="#">Read More ></a>
                </div>
                <div class="col py-5 me-4">
                    <i class="fa-solid fa-video mb-4 fs-3"></i>
                    <h4 class="mb-3">Brand Strategy</h4>
                    <p>Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.</p>
                    <a href="#">Read More ></a>
                </div>
                <div class="col py-5 me-4">
                    <i class="fa-solid fa-droplet mb-4 fs-3"></i>
                    <h4 class="mb-3">Local SEO</h4>
                    <p>Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.</p>
                    <a href="#">Read More ></a>
                </div>
                <div class="col py-5">
                    <i class="fa-solid fa-droplet mb-4 fs-3"></i>
                    <h4 class="mb-3">SEO Analysis</h4>
                    <p>Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.</p>
                    <a href="#">Read More ></a>
                </div>
           </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.what-we-do {
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

            .fa-solid {
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