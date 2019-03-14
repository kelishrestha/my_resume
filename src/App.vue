<template>
  <v-app id="resume">
    <SideBar name="Kelina Shrestha" email="kelishrestha97@gmail.com"/>
    <v-content>
      <DetailComponent/>
    </v-content>
  </v-app>
</template>

<script>
import SideBar from './components/SideBar'
import DetailComponent from './components/DetailComponent'

export default {
  name: 'App',
  components: {
    SideBar,
    DetailComponent
  },
  data () {
    return {
      //
    }
  }
}
</script>

<style scoped>
  .parallax-height {
    height: 100vh;
  }
</style>
