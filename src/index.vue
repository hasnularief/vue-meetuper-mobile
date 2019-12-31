<template>
  <view class="container">
    <navigation />
  </view>
</template>

<script>
  import Navigation from './navigation'
  import Vue from 'vue-native-core'
  import { VueNativeBase } from 'native-base'

  Vue.use(VueNativeBase)

  export default {
    components: {
       Navigation
    },

    data() {
      return {
        
      }
    },
  }
</script>

<style>
  .container {
    padding: 40px;
    flex: 1;
  }
</style>
