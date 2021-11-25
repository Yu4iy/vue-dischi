<template>
	<div class="card">
		<img :src="poster" :alt="title">
		<div class="info">
			<h2 class="info__title">{{title}}</h2>
			<div class="info__author">{{author}}</div>
			<div class="info__genre">{{genre}}</div>
			<div class="info__year">{{year}}</div>
		</div>
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

<style lang="scss" scoped>
@import '@/styles/global.scss';
.card{
	background: $headColor;
	width: 190px;
	padding: 1.2rem ;
	margin: 1.1rem;
	display: flex;
	flex-direction: column;

	
	img{
		max-width: 150px;
		min-height: 150px;
	}
	.info{
		display: flex;
		flex-direction: column;
		text-align: center;
		.info__title {
			font-size: 1rem;
			color: $whiteColor;
			text-transform: uppercase;
			margin: 2rem 0;
		}
		.info__author {
			font-size: 0.9rem;
			color: $ColorLightGray;
			
		}
		.info__genre {
			font-size: 0.8rem;
			color: $ColorLightGray;
			margin: 1rem 0;

		}
		.info__year {
			font-size: 0.8rem;
			color: $whiteColor;
		}
	}
}
</style>