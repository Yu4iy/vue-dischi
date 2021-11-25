<template>
  <div id="app">
   <section class="main-section">
      <Header/>
      <MusList/>
  </section>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import MusList from '@/components/MusList.vue'
export default {
  name: 'App',
  components: {
    Header,
    MusList
  }
}
</script>

<style lang="scss">
@import '@/styles/global.scss';
  .main-section{
    height: 100vh;
  }
</style>
