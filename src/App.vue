<template>
  <div id="app">
    <Header/>
    <MainContent/>
    <AboutContent/>
    <ThemesContent/>
    <Members/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/header/Header';
import MainContent  from './components/main/MainContent';
import Footer from './components/footer/Footer';
import AboutContent from "@/components/main/AboutContent";
import ThemesContent from "@/components/main/ThemesContent";
import Members from "@/components/main/Members";

export default {
  name: 'App',
  components: {
    Header,
    MainContent,
    AboutContent,
    ThemesContent,
    Members,
    Footer
  },
  mounted() {
    window.addEventListener('beforeunload', this.scrollToTop);
  },
  methods: {
    scrollToTop() {
      window.scrollTo(0, 0);
    }
  },
  beforeUnmount() {
    window.removeEventListener('beforeunload', this.scrollToTop);
  }
}
</script>

<style scoped>

</style>
