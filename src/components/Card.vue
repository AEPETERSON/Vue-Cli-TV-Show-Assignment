
<!--Name:Alex Peterson-->
<!--Date: 12/7/2020-->
<template>
  <div>
      <h1>{{aShow.name}}</h1>
      <img v-bind:src="'https://image.tmdb.org/t/p/w500/' + aShow.poster_path">
      <p>{{aShow.overview}}</p>

  </div>
</template>

<script>
// import axios from 'axios'
export default {
  name: 'Card',
  props: ['aShow']

}

</script>
