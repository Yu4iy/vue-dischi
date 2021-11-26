<template>
  <div>
	<span class="wavy">
		<div>loading</div>
	</span>
  </div>
</template>

<script>
export default {
name:'Loader'
}
</script>

<style lang="scss" scoped>
@import '@/styles/global.scss';
	div{
		position: fixed;
		left: 50%;
		top: 50%;
		transform: translate(-50%, -50%);
		.wavy{
			position: relative;
			width: 150px;
			height: 50px;
			overflow: hidden;
			display: block;
			border-radius: 50px;
			>div{
				text-align: center;
				color: $whiteColor;
				text-transform: uppercase;
				letter-spacing: 3px;
			}
			&::before{
				content: 'aaaaaaaaaaaaaaa';
				
				position: absolute;
				color: transparent;
				font-size: 2rem;
				text-decoration-style: wavy;
				text-decoration-line: underline;
				text-decoration-color: $whiteColor;
				animation: wavy linear 2s infinite;
			}
		}
	}
	@keyframes wavy {
		0%{
			translate: -0px;
		}
		100%{
			translate: -45px;

		}
	}
</style>