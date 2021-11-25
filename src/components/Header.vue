<template>
  <div>
    <img src="../assets/logo.png" alt="">
  </div>
</template>

<script>
export default {
name:'Header'
}
</script>

<style lang = 'scss' scoped>
@import '@/styles/global.scss';

  div{
    padding: 10px;
    width: 100%;
    background-color: $headColor;
    position: fixed;
    img{
      max-width: 40px;
      }
    
  }
</style>