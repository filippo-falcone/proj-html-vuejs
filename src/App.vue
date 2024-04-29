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
        button: false,
        href: '#'
      },
      {
        name: 'Who We Are',
        button: false,
        href: '#who-we-are'
      },
      {
        name: 'What We Do',
        button: false,
        href: '#what-we-do'
      },
      {
        name: 'What We Work',
        button: false,
        href: '#what-we-work'
      },
      {
        name: 'Careers',
        button: false,
        href: '#plans'
      },
      {
        name: 'News',
        button: false,
        href: '#news'
      },
      {
        name: 'Get in Touch Now',
        button: true,
        href: '#contact-us'
      }
      ],
      isShow: '',
      isActive: ''
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
    onscroll = () => {
      this.showButtonToScroll();
      if (scrollY > 700) {
          this.isActive = 'active';
      } else {
          this.isActive = '';
      }
    }
  }
}
</script>

<template>
  <PageHeader :linksInfo="links" :isActive="isActive"></PageHeader>
  <PageMain></PageMain>
  <PageFooter :linksInfo="links"></PageFooter>
  <button class="scroll-up btn small brand-dark" :class="isShow" @click="scrollTop">
    <i class="fa-solid fa-chevron-up"></i>  
  </button>
</template>

<style lang="scss">
@use './style/generic.scss';

.scroll-up {
  display: none;
  position: fixed;
  bottom: 0;
  right: 2.5rem;
  z-index: 1;

  &.active {
      display: block;
  }
}
</style>