<template>
  <div id="app">
      <myHeader></myHeader> 
      <myMain></myMain>
      <myLinkBox></myLinkBox>
      <myFooter></myFooter>
  </div>
</template>

<script>
import myHeader from './components/myHeader.vue'
import myMain from './components/myMain.vue'
import myLinkBox from './components/myLinkBox.vue'
import myFooter from './components/myFooter.vue'

export default {
  name: 'App',
  components: {
    myHeader,
    myMain,
    myLinkBox,
    myFooter,
  }
}
</script>

<style lang="scss">
  @import "./assets/style/general.scss";
    
</style>
