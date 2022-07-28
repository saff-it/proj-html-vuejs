<template>
  <div id="app">
    <siteHeader />
    <siteMain />
    <siteFooter />

  </div>
</template>

<script>
import siteHeader from './components/siteHeader.vue'
import siteMain from './components/siteMain.vue'
import siteFooter from './components/siteFooter.vue'


export default {
  name: 'App',
  components: {
    siteHeader,
    siteMain,
    siteFooter,

  },

  
}
</script>



<style lang="scss">
@import "~bootstrap/scss/bootstrap.scss";
@import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@1.9.1/font/bootstrap-icons.css");

@import "./styles/general.scss";
@import "./styles/variables.scss";




</style>
