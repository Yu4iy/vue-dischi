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
    background-color: $headColor;
    img{max-width: 40px;}
  }
</style>