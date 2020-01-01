<template>
  <root>
    <app-navigator></app-navigator>
  </root>
</template>

<script>
  import { Root } from "native-base";
  import HomeScreen from '@/screens/HomeScreen.vue'
  import Screen1 from '@/screens/Screen1.vue'
  import Screen2 from '@/screens/Screen2.vue'
  import Screen3 from '@/screens/Screen3.vue'

  /*
  import {
    createAppContainer,
    createStackNavigator,
    createBottomTabNavigator
  } from "vue-native-router"

  */

  import { createAppContainer } from 'react-navigation'
  import { createStackNavigator } from 'react-navigation-stack'
  import { createBottomTabNavigator } from 'react-navigation-tabs'

  const StackNavigator = createStackNavigator({
    Home: HomeScreen,
    Screen1,
  }, {
    initialRouteName: 'Home',

  })

  const SomeOtherStack = createStackNavigator({
    Screen2,
    Screen3
  })

  const TabNavigator = createBottomTabNavigator({
    Meetups: StackNavigator,
    Other: SomeOtherStack
  })

  const AppNavigator = createAppContainer(TabNavigator)

  export default {
    components: {
       Root, AppNavigator
    },

    data() {
      return {
        
      }
    },
  }
</script>