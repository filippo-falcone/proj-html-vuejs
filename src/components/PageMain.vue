<script>
import AppClients from './AppClients.vue';
import AppContact from './AppContact.vue';
import AppHero from './AppHero.vue';
import AppNews from './AppNews.vue';
import AppPlans from './AppPlans.vue';
import AppWeAre from './AppWeAre.vue';
import AppWeDo from './AppWeDo.vue';
import AppWork from './AppWork.vue';

export default {
    components: {
        AppClients,
        AppContact,
        AppHero,
        AppNews,
        AppPlans,
        AppWeAre,
        AppWeDo,
        AppWork
    }
}
</script>

<template>
    <AppHero></AppHero>
    <AppWeAre></AppWeAre>
    <AppWeDo></AppWeDo>
    <AppWork></AppWork>
    <AppPlans></AppPlans>
    <AppNews></AppNews>
    <AppClients></AppClients>
    <AppContact></AppContact>
</template>

<style scoped lang="scss"></style>