<template>
  <div id="app">
    <CircleProgress :progressOption = "progressOption"/>
  </div>
</template>

<script>

import CircleProgress from './components/circle.vue'
export default {
  name: 'App',
  data(){
    return {
        progressOption:{
          progressColor: 'red',
          strokeWidth:20,
          radius:100,
          progress:50,
          text:"50%",
          animate:true
        }
    }
  },
  components: {
    CircleProgress
  },
}
</script>

<style lang="less">
#app {
  text-align: center;
  margin-top:100px;
}
</style>
