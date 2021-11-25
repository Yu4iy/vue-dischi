<template>
	<section>
		<div class="music-cards">
			
			<MusicList/>
		</div>
	</section>
</template>

<script>
import MusicList from '@/components/MusicList.vue';
export default {
name:'Main',
components:{
	MusicList,
}
}
</script>

<style lang="scss" scoped>
@import '@/styles/global.scss';
	section{
		background: $bodyColor;
		height: calc(100% - 68px);
		padding: 120px 75px 0;
		overflow: auto;
			
	}
</style>