<!--Name:Alex Peterson-->
<!--Date: 12/7/2020-->
<template>
  <div id="app">
    
    <Card v-for="show in shows" v-bind:key="show.id" v-bind:aShow="show"></Card>
    <Header msg="Popular TV Shows"></Header>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Card from './components/Card.vue'
import axios from 'axios'
export default {
  name: 'App',
  components: {
    Header,Card
  },
   data()
  {
      return{
        shows:
        [
              //{id:0, title:"", poster:"",overview:""}

        ]
      }
      


  },
  mounted()
  {
      axios.get('https://api.themoviedb.org/3/tv/popular?api_key=6b13127c67404e56318dfe068967a8e8&language=en-US&page=1')
      .then((response) =>{
          this.shows = response.data
          

      })
      //console.log(this.shows);
  }
}


</script>

<style>
body{
  background-color:gold;
}
h1{
  background-color: silver;
  text-align: center;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color:black;
  margin-top: 60px;
  
  
}
</style>
