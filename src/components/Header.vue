<template>
	<div>
		<img src="../assets/logo.png" alt="">
		
		<select v-model = 'input' @change = "$emit('chiose', input)" name="gen" id="gen">
			<option value="">Tutti Brnai</option>
			<option value="Rock">Rock</option>
			<option value="Pop">Pop</option>
			<option value="Metal">Metal</option>
			<option value="Jazz">Jazz</option>
		</select>
	</div>
</template>

<script>
export default {
name:'Header',
data(){
	return{
		input:''
	}
}
}
</script>

<style lang="scss" scoped>
@import '@/styles/global.scss';
div{
	display: flex;
	align-items: center;
	justify-content: space-between;
	background: $headColor;
	img{
		width: 45px;
		margin: 10px 0 10px 10px;
	}
	select{
		width: 200px;
		height: 40px;
		margin: 1rem;
	}
}
</style>