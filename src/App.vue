<template>
  <div id="app">
   <section class="main-section">
      <Header/>
      <Main/>
  </section>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Main from '@/components/Main.vue'
export default {
  name: 'App',
  components: {
    Header,
    Main,
  }
}
</script>

<style lang="scss">
@import '@/styles/global.scss';
 
</style>
