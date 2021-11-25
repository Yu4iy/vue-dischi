<template>
	<div>
		<div v-for="(item,index) in musicList" :key="index">
			<Card
			:poster = item.poster
			:title = item.title
			:author = item.author
			:genre = item.genre
			:year = item.year
			/>
		</div>	
	</div>	
</template>

<script>
import axios from 'axios'
import Card from '@/components/Card.vue'

export default {
name:'MusList',
data() {
	return{
		
		musicList: null,
	}
},
created(){
	this.list()
},
methods:{
	list(){
		axios.get('https://flynn.boolean.careers/exercises/api/array/music').then(result => {
			this.musicList = result.data.response
		})
		.catch(err => console.log(err))
	}
},
components:{
Card,
}
}

</script>

<style lang="scss" scoped>
	div{
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
	}
</style>