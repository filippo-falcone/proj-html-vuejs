<script>
import PageHeader from './components/PageHeader.vue';
import PageMain from './components/PageMain.vue';

export default {
  components: {
    PageHeader,
    PageMain
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
  <PageMain></PageMain>
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