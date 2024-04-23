<script>
export default {}
</script>

<template>
    <section class="clients">
        <div class="container text-center">
            <div class="row justify-content-center">
                <div class="col-7">
                    <h3 class="mb-5">What Our  Clients Say</h3>
                    <div class="img-container my-4">
                        <img src="../assets/images/testimonials-2.jpg" alt="">
                    </div>
                    <i>Ability proceeds from a fusion of skills, knowledge, understanding and imagination, consolidated by ecperience.</i>
                    <div class="my-4">
                        <strong>Luis Desalvo</strong>
                        <span class="text-uppercase">, creo tech</span>
                    </div>
                    <div class="points-container d-flex justify-content-center">
                        <div class="point me-2"></div>
                        <div class="point active"></div>
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
                    background-color: $brand-dark;
                    border-radius: 50%;
                    
                    &.active {
                        background-color: transparent;
                        border: 1px solid $brand-dark;
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