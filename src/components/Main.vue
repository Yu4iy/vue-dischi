<template>
  <section>
    <ul>
      <li>
          <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
          <h2 class="title">New Jersy</h2>
          <h3 class="band">Bon Jovi</h3>
          <div class="year">2018</div>
          <div class="type">rock</div>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
name:'Main'
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
ul{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  
  li{
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
    margin: 15px;
    background-color: #2e3a46;
   
    img{
      max-width: 150px;
    }
  }
 } 
</style>