<template>
  <view class="container">
    <text class="text-color-primary">{{ title }}</text>
    <button title="Go to screen 1" @press="goToScreen1()" />
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
        title: 'Home Screen'
      }
    },

    methods: {
      goToScreen1() {
        this.navigation.navigate('Screen1')
        
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
