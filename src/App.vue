<script>
import PageHeader from './components/PageHeader.vue';

export default {
  components: {
    PageHeader
  },
  data() {
    return {
      links: [
      {
        name: 'Home',
      },
      {
        name: 'Who We Are'
      },
      {
        name: 'What We Do'
      },
      {
        name: 'What We Work'
      },
      {
        name: 'Careers'
      },
      {
        name: 'News'
      },
    ]
    };
  } 
}
</script>

<template>
  <PageHeader :linksInfo="links"></PageHeader>
</template>

<style lang="scss">
@use './style/generic.scss';
</style>