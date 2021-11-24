<template>
  <div id="app">
    <Header  v-if="LoadingCheck" />
    <router-view/>
    <Footer  v-if="LoadingCheck" />
  </div>
</template>

<script>
import EventBus from '@/utils/EventBus';

import Header from '@/components/Header'
import Footer from '@/components/Footer'
export default {
  name: 'App',
  components: {
    Header, 
    Footer
  },

  data(){
     return{
        LoadingCheck: false,
      }
  },
   created(){
      EventBus.$on('Loading-end', (payload)=>{
          this.LoadingCheck = payload; 
          console.log( this.LoadingCheck);
      });
  }
} 
</script>

<style lang="scss">
@import '@/assets/scss/_reset.scss';  

#app { 
  margin:0; padding:0;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center; 
  color: #2c3e50;
}
</style>
