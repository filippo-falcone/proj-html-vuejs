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
      ],
      isShow: ''
    };
  },
  methods: {
    showButtonToScroll() {
      if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
        this.isShow = 'active';
      } else {
        this.isShow = '';
      }
    },
    scrollTop() {
      document.body.scrollTop = 0;
      document.documentElement.scrollTop = 0;
    }
  },
  mounted() {
    window.onscroll = () => {
      this.showButtonToScroll();
    }
  }
}
</script>

<template>
  <PageHeader :linksInfo="links"></PageHeader>
  <PageMain></PageMain>
  <PageFooter :linksInfo="links"></PageFooter>
  <button class="btn small brand-dark" :class="isShow" @click="scrollTop">
    <i class="fa-solid fa-chevron-up"></i>  
  </button>
</template>

<style lang="scss">
@use './style/generic.scss';
@use './style/partials/variables' as *;

p {
  color: $brand-dark-light;
}

.btn {
  &.small{
    &.brand-dark {
      width: 2.3125rem;
      height: 1.75rem;
      background-color: $brand-dark;
      border-color: transparent;
      border-radius: 0.375rem 0.375rem 0 0;
      color: $brand-light-tertiary;
      font-size: 10px;
      display: none;
      position: fixed;
      bottom: 0;
      right: 40px;
      z-index: 1;

      &.active {
        display: block;
      }

      &:hover {
        background-color: $brand-dark-light;
      }
    }

    
  }

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