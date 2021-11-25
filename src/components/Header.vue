<template>
	<div>
		<img src="../assets/logo.png" alt="">
	</div>
</template>

<script>
export default {
name:'Header',
}
</script>

<style lang="scss" scoped>
@import '@/styles/global.scss';
div{
	background: $headColor;
	img{
		width: 45px;
		margin: 10px 0 10px 10px;
	}
}
</style>