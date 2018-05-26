<template>
  <div id="app">
    <Head/>
    <Intro v-show="showIntro"></Intro><Picture v-show="showPic"/><News v-show="showNews"/><Contact v-show="showCont"/>
    <Intro v-if="flag==2"/>
    <Picture v-if="flag==3"/>
    <News v-if="flag==4"/>
    <Contact v-if="flag==4"/>
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
  data(){
    return{
      flag : 0,
      showIntro : true,
      showPic : true,
      showNews : true,
      showCont : true
    }
  },
  components: {
    Head,
    Intro,
    Picture,
    News,
    Contact
  },
  mounted(){
    window.addEventListener('scroll',this.handleScroll)
  },
  methods:{
    handleScroll:function () {
      var scrollTop = window.pageYOffset || window.documentElement.scrollTop || document.body.scrollTop;
      console.log(scrollTop)
      if(scrollTop <= 620){
        console.log(this.flag)
      } else if(scrollTop > 620 && scrollTop < 1315){
        this.flag=2
        this.showIntro = false
        this.showPic = true
        this.showNews = true
        this.showCont = true
        console.log(this.flag)
      }else  if(scrollTop > 1315 && scrollTop < 2093){
        this.flag=3
        this.showIntro = true
        this.showPic = false
        this.showNews = true
        this.showCont = true
      } else  if(scrollTop > 2093 && scrollTop < 2660){
        this.flag=4
        this.showIntro = true
        this.showPic = true
        this.showNews = false
        this.showCont = false
      }
    }
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
