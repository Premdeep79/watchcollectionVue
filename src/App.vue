<template>
  <MyHeader appName="Watch Collection"/> 
  <WatchesList :watches=watches />
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import WatchesList from './components/WatchesList.vue'


export default{
  name: 'App',
  components:{
    MyHeader,
    WatchesList
  },
  data(){
    return {
      watches: []
    }
  },
  methods:{
    async fetchWatches(){
      const res = await fetch('https://watchescollectionnode.onrender.com/api');
      const data = await res.json()
      console.log(data)
      return data.watches;
    }
  },
  async created(){
      this.watches = await this.fetchWatches();
  }
}
</script>


<style>

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: sans-serif;
}

#app{
  background-color: darkslategray;
}
</style>
