<template>
    <div id="loading">
        <button v-on:click="clickBtn">HelloWorld</button>
    </div>
</template>

<script>

import EventBus from '../utils/EventBus';
export default {
  name: 'Loading',
  components:{
  },
  data(){
    return{
      isComponent : true,
    }
  },
  methods:{
    clickBtn(){
      EventBus.$emit('Loading-end', true );
    },
  }
}
</script>

<style lang="scss" scoped>

</style>