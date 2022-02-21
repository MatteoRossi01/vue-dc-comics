<template>
  <div id="app">
      <myHeader></myHeader> 
      <myMain></myMain>
      <myLinkBox></myLinkBox>
  </div>
</template>

<script>
import myHeader from './components/myHeader.vue'
import myMain from './components/myMain.vue'
import myLinkBox from './components/myLinkBox.vue'

export default {
  name: 'App',
  components: {
    myHeader,
    myMain,
    myLinkBox,
  }
}
</script>

<style lang="scss">
  @import "./assets/style/general.scss";
    
</style>
