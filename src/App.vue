<template>
  <img alt="Vue logo" src="./assets/logo11.png">
  <HelloWorld msg="Welcome Metaverse"/>
  <Home />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Home from './components/Home.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
     Home
  }
}
</script>


