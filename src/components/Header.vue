<!--Name:Alex Peterson-->
<!--Date: 12/7/2020-->
<template>
  <body>
    <div>
      <h1>{{msg}}</h1>
    </div>
  </body>
</template>

<script>
export default {
  name: 'Header',
  props: {
    msg: String
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
