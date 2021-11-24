<template>
  <header >
    <p>해더영역</p>
  </header>
</template>

<script>
export default {
  name: 'Header',
  props:{
  },
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  header{ padding:20px;
    h1{ float: left;}
 
  }
</style>
