<template>
  <div>
	
  </div>
</template>

<script>
import axios from 'axios'

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

}
}

</script>

<style>

</style>