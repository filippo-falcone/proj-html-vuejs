<script>
import AppHero from './AppHero.vue';
import AppNews from './AppNews.vue';
import AppPlans from './AppPlans.vue';
import AppWeAre from './AppWeAre.vue';
import AppWeDo from './AppWeDo.vue';
import AppWork from './AppWork.vue';

export default {
    components: {
        AppHero,
        AppWeAre,
        AppWeDo,
        AppWork,
        AppPlans,
        AppNews
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
</template>

<style scoped lang="scss"></style>