<template>
	<div>
		<div v-if = "MusList !== null" class="cards">
			<div v-for="(item, index) in MusList" :key = "`item-${index}`">
				<Card
					:poster	=	item.poster
					:title	=	item.title
					:author	=	item.author
					:genre	=	item.genre
					:year	=	item.year
				/>
			</div>
		</div>
		<div v-else class="loader">
			<Loader/>
		</div>

	</div>
</template>

<script>
import Card from '@/components/Card.vue'
import Loader from '@/components/Loader.vue'
export default {
name:'MusicList',
components:{
	Card,
	Loader
},
data(){
	return{
		
	
	}
},

created(){

},

methods:{


},
props:{
	MusList:Array
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