<template>
  <div class="card">
			<img :src="poster" alt="">
         <h2 class="title">{{title}}</h2>
         <h3 class="band">{{author}}</h3>
         <div class="year">{{year}}</div>
         <div class="type">{{genre}}</div>
  </div>
</template>

<script>
export default {
name:'Card',
props:{
	poster:String,
	title:String,
	author:String,
	genre:String,
	year:String,
}
}
</script>

<style lang = 'scss' scoped>
@import '@/styles/global.scss';
  .card{
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
    margin: 15px;
    max-width: 200px;
    background-color: #2e3a46;
   
	img{
      max-width: 150px;
    }
	h2{
		text-align: center;
		margin: 1.5rem 0;
		color: $whiteColor;
		text-transform: uppercase;
		font-weight: 500;
		font-size: 1rem;
	}
	h3{
		color: $ColorLightGray;
		font-size: 0.8rem;

	}
	.year{
		color: $ColorLightGray;
		margin: 0.8rem 0;
	}
	.type{
		font-size: 0.8rem;
		color: $whiteColor;
	}
  }
 
</style>