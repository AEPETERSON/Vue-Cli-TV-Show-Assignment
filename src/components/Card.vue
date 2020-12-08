
<!--Name:Alex Peterson-->
<!--Date: 12/7/2020-->
<template>
  <div>
    <h1>Happy Birthday</h1>
      <h2>{{aShow.name}}</h2>
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
