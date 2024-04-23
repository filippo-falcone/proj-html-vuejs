<script>
export default {}
</script>

<template>
    <section id="contact-us">
        <div class="opacity"></div>
        <div class="contact-container d-flex flex-column justify-content-center align-items-center text-center">
            <div class="text">
                <h3 class="mb-4">Start Your Free Consultation</h3>
                <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.</p>
            </div>
            <div class="btn-container pt-4">
                <button class="btn big brand-primary rounded-pill me-3">contact us now</button>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

#contact-us {
    min-height: 23.875rem;
    background-image: url(../assets/images/CTA-seo-1.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    position: relative;
    
    .contact-container {
        background-color: #00000084;
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;

        .text {
            width: 40%;
            color: $brand-light-tertiary;
            
            p {
                color: $brand-light-tertiary;
            }
        }
    }
}
</style>