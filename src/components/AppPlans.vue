<script>
export default {}
</script>

<template>
    <section class="plans">
        <div class="container text-center">
            <div class="row g-5">
                <div class="col-12 d-flex justify-content-center">
                    <div class="text">
                        <h3 class="mb-4">Our Work</h3>
                        <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.</p>
                    </div>
                 </div>
                 <div class="col d-flex flex-column align-items-center py-5 me-4">
                    <h4 class="mb-3">Standard</h4>
                    <div class="price-container d-flex align-items-center py-3">
                        <div class="value">$</div>
                        <div class="price fs-1">19</div>
                        <div>
                            <div class="price cent text-start">99</div>
                            <div class="month">monthly</div>
                        </div>
                    </div>
                    <div class="pojects py-3">5 Projects</div>
                    <div class="storage py-3">5 GB Storage</div>
                    <div class="usage py-3">Unlimited Users</div>
                    <div class="btn-container py-3">
                        <button class="btn big brand-outline-dark rounded-pill">start today</button>
                    </div>
                </div>
                 <div class="col d-flex flex-column align-items-center py-5 me-4">
                    <h4 class="mb-3">Premium</h4>
                    <div class="price-container d-flex align-items-center py-3">
                        <div class="value">$</div>
                        <div class="price fs-1">29</div>
                        <div>
                            <div class="price cent text-start">99</div>
                            <div class="month">monthly</div>
                        </div>
                    </div>
                    <div class="pojects py-3">10 Projects</div>
                    <div class="storage py-3">15 GB Storage</div>
                    <div class="usage py-3">Unlimited Users</div>
                    <div class="btn-container py-3">
                        <button class="btn big brand-outline-dark rounded-pill">start today</button>
                    </div>
                </div>
                 <div class="col d-flex flex-column align-items-center py-5 me-4">
                    <h4 class="mb-3">Professional</h4>
                    <div class="price-container d-flex align-items-center py-3">
                        <div class="value">$</div>
                        <div class="price fs-1">39</div>
                        <div>
                            <div class="price cent text-start">99</div>
                            <div class="month">monthly</div>
                        </div>
                    </div>
                    <div class="pojects py-3">15 Projects</div>
                    <div class="storage py-3">30 GB Storage</div>
                    <div class="usage py-3">Unlimited Users</div>
                    <div class="btn-container py-3">
                        <button class="btn big brand-outline-dark rounded-pill">start today</button>
                    </div>
                </div>
                 <div class="col d-flex flex-column align-items-center py-5 me-4">
                    <h4 class="mb-3">Extreme</h4>
                    <div class="price-container d-flex align-items-center py-3">
                        <div class="value">$</div>
                        <div class="price fs-1">59</div>
                        <div>
                            <div class="price cent text-start">99</div>
                            <div class="month">monthly</div>
                        </div>
                    </div>
                    <div class="pojects py-3">Unlimited Projects</div>
                    <div class="storage py-3">Unlimited Storage</div>
                    <div class="usage py-3">Unlimited Users</div>
                    <div class="btn-container py-3">
                        <button class="btn big brand-outline-dark rounded-pill">start today</button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.plans {
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
                    padding-top: 13px ;
                    font-size: .875rem;
                    align-self: flex-start;
                }

                .price {
                    color: $brand-secondary;

                    &.cent {
                         font-size: 14px;
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