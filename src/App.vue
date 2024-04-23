<script>
import PageFooter from './components/PageFooter.vue';
import PageHeader from './components/PageHeader.vue';
import PageMain from './components/PageMain.vue';

export default {
  components: {
    PageFooter,
    PageHeader,
    PageMain
  },
  data() {
    return {
      links: [
      {
        name: 'Home',
        button: false
      },
      {
        name: 'Who We Are',
        button: false
      },
      {
        name: 'What We Do',
        button: false
      },
      {
        name: 'What We Work',
        button: false
      },
      {
        name: 'Careers',
        button: false
      },
      {
        name: 'News',
        button: false
      },
      {
        name: 'Get in Touch Now',
        button: true
      }
    ]
    };
  } 
}
</script>

<template>
  <PageHeader :linksInfo="links"></PageHeader>
  <PageMain></PageMain>
  <PageFooter :linksInfo="links"></PageFooter>
</template>

<style lang="scss">
@use './style/generic.scss';
@use './style/partials/variables' as *;

p {
  color: $brand-dark-light;
}

.btn {
  &.big {
    &.brand-primary {
      background-color: $brand-primary;
      color: $brand-light-secondary;
  
      &:hover {
        background-color: transparent;
        border: 1px solid $brand-primary;
        color: $brand-primary;
      }
    }

    &.brand-secondary {
      background-color: $brand-secondary;
      color: $brand-light-secondary;
  
      &:hover {
        background-color: transparent;
        border: 1px solid $brand-secondary;
        color: $brand-secondary;
      }
    }

    &.brand-outline-dark {
      border: 1px solid $brand-dark;
      color: $brand-dark;

      &:hover {
        border: 1px solid $brand-secondary;
        color: $brand-secondary;
      }
    }
  }
}
</style>