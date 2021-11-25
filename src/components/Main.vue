<template>
  <section>
          <!-- <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
          <h2 class="title">New Jersy</h2>
          <h3 class="band">Bon Jovi</h3>
          <div class="year">2018</div>
          <div class="type">rock</div> -->
        <MusList/>
  </section>
</template>

<script>
import MusList from '@/components/MusList.vue'

export default {
name:'Main',
components:{
  MusList
}
}
</script>

<style lang="scss" scoped>
@import '@/styles/global.scss';
  section{
    background-color: $bodyColor;
    padding: 110px 50px;
    height: 100vh;
    overflow: auto;
  }

</style>