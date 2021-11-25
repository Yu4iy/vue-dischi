<template>
	<div class="cards">
		<div v-for="(item, index) in list" :key = "`item-${index}`">
			<Card
				:poster	=	item.poster
				:title	=	item.title
				:author	=	item.author
				:genre	=	item.genre
				:year	=	item.year
			/>
		</div>
	</div>

</template>

<script>
import axios from 'axios'
import Card from '@/components/Card.vue'
export default {
name:'MusicList',
components:{
	Card,
},
data(){
	return{

		list:null
	}
},

created(){
	this.getMusicList()
},

methods:{
	getMusicList(){
		axios
		.get('https://flynn.boolean.careers/exercises/api/array/music')
		.then(response => (this.list = response.data.response))
		
	}

}

}
</script>

<style lang="scss" scoped>
@import '@/styles/global.scss';
.cards{
	display: flex;
	flex-wrap: wrap;
	justify-content: center;
	align-items: stretch;
	>div{
		display: flex;
	}
}

</style>