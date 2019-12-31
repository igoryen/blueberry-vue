<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Blueberry app"/>
    <EventsWrapper/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import EventsWrapper from './components/EventsWrapper.vue'


export default {
  name: 'app',
  components: {
    HelloWorld,
    EventsWrapper
  }
}
</script>

<style lang="scss">
body {
    background-color: #2c3e50;
    color: #f2f2f2;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  
  margin-top: 60px;
}
</style>
