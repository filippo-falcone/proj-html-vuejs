<script>
export default {
    data() {
        return {

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
                <div class="col py-5 me-4">
                    <i class="fa-solid fa-road mb-4 fs-3"></i>
                    <h4 class="mb-3">Establish Goals</h4>
                    <p>Aliquam non elit lacus. Praesent aliquet, ipsum id scelerisque convallis, mi ligula euismond odio, vel dictum mi risus a mi.</p>
                </div>
                <div class="col py-5 me-4">
                    <i class="fa-solid fa-video mb-4 fs-3"></i>
                    <h4 class="mb-3">Work With a Team</h4>
                    <p>Cras semper auctor aliquam. Sed porta sed lacus sit amet consectetur. Lorem ipsum dolor sit amet, consectetur adipiscin.</p>
                </div>
                <div class="col py-5">
                    <i class="fa-solid fa-droplet mb-4 fs-3"></i>
                    <h4 class="mb-3">Establish Goals</h4>
                    <p>Aliquam non elit lacus. Praesent aliquet, ipsum id scelerisque convallis, mi ligula euismond odio, vel dictum mi risus a mi.</p>
                </div>
           </div>
           <div>
                <img src="../assets/images/agency-seo-desk-front.jpg" alt="">
           </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
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

            .fa-solid {
                color: $brand-primary;
            }
        }
    }
}
</style>