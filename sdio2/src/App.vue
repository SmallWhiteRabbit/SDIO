<template>
  <div id="app">
    <Head/>
      <Intro/>
    <Picture/>
    <News/>
    <Contact/>
  </div>
</template>

<script>
import Head from './components/Head'
import Intro from  './components/Intro'
import Picture from  './components/Picture'
import News from  './components/News'
import Contact from './components/Contact'

export default {
  name: 'App',
  components: {
    Head,
    Intro,
    Picture,
    News,
    Contact
  }
}

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

</style>
