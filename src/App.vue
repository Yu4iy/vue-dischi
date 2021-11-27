<template>
  <div id="app">
    <Header
     @chiose='test'
      />
    <section class="main">
      <MusicList
      :MusList = filter
      />      
    </section>
  </div>
</template>

<script>
import axios from 'axios'
import Header from '@/components/Header.vue'
import MusicList from '@/components/MusicList.vue';

export default {
  name: 'App',
  data(){
    return{
      
      list:null,
      input:''
    }
  },

  created(){
    this.getMusicList()
  },
  computed:{
    filter(){
      if(this.input === ''){
        return this.list;
      }
      return this.list.filter(m => {
        return m.genre.includes(this.input)
      })
    }

  },
  methods:{
    getMusicList(){
      axios
      .get('https://flynn.boolean.careers/exercises/api/array/music')
      .then(response => (this.list = response.data.response))
      
    },

    test(el){
      this.input = el
    }
   

  },
  components: {
    Header,
    MusicList,
  }

}
</script>

<style lang="scss">
@import '@/styles/global.scss';
#app{
  height: 100vh;
  .main{
		background: $bodyColor;
		height: calc(100% - 72px);
		padding: 120px 75px 0;
		overflow: auto;
			
	}
}
</style>
