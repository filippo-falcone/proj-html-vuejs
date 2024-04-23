<script>
export default {}
</script>

<template>
    <section class="consultation">
        <div class="container d-flex flex-column align-items-center text-center">
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

.consultation {
    padding-top: 6.25rem;
    padding-bottom: 6.25rem;
    background-image: url(../assets/images/CTA-seo-1.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    
    .container {
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