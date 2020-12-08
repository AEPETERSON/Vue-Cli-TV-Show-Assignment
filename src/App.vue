<!--Name:Alex Peterson-->
<!--Date: 12/7/2020-->
<template>
  <body>
  
  <div id="app">
      <Header id="appTitle" msg="Popular TV Shows"></Header>
      <Card v-for="show in shows.slice(0,4)" v-bind:key="show.id" v-bind:aShow="show"></Card>
  </div>
  </body>
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
          this.shows = response.data.results
          

      })
      //console.log(this.shows);
  }
}


</script>

<style>
#appTitle{
  background-color: silver;
  text-align: center;
  font-size: 80px;

}
body{
  background-color:gold;
}
h1{
  background-color: silver;
  font-size: 50px;
}
p{
  background-color: purple;
  font-size: 40px;
  color: white;
  
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color:black;
  margin-top: 60px;
  
  
}
</style>
