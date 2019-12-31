<template>
  <view class="container">
    <text class="text-color-primary">{{ title }}</text>
    <button title="Go to screen 21" @press="goToScreen2()" />
  </view>
</template>

<script>
  export default {

    props: {
      navigation: {
        type: Object
      }
    },

    data() {
      return {
        title: 'Screen 1'
      }
    },

    methods:{
      goToScreen2() {
        this.navigation.navigate('ScreenTwo')
        
      }
    }
  }
</script>

<style>
  .text-color-primary {
    color: blue;
  }
  .container {
    background-color: white;
    align-items: center;
    justify-content: center;
    flex: 1;
  }
</style>
