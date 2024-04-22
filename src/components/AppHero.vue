<script>
export default {}
</script>

<template>
    <section class="hero">
        <div class="container h-100">
            <div class="row align-items-center h-100">
                <div class="col-6">
                    <h1>SEM Campaigns Made Simple With Avada</h1>
                    <p class="my-4">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Phasellus eu ornare erat. Curabitur pulvinar elit.</p>
                    <div class="btn-container">
                        <button class="btn big brand-secondary rounded-pill me-3">get in touch now</button>
                        <button class="btn big brand-primary rounded-pill">get in touch now</button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.hero {
    height: 100vh;
    margin-top: -4.1875rem;
    background-image: url(../assets/images/1-hero-image.png);
    background-size: 100%;
    background-repeat: no-repeat;
    color: $brand-light;
}
</style>