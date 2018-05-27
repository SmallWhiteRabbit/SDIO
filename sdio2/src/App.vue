<template>
  <div id="app">
    <Head/>
    <Intro :msg="showIntro" ></Intro>
    <Picture :msg="showPic" />
    <News :msg="showNews"/>
    <Contact :msg="showCont" />
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
      showIntro : false,
      showPic : false,
      showNews : false,
      showCont : false
    }
  },
  components: {
    Head,
    Intro,
    Picture,
    News,
    Contact
  },
  created(){
    window.addEventListener('scroll',this.handleScroll)
    // this.handleScroll()
  },
  methods:{
    handleScroll:function () {
      var scrollTop = window.pageYOffset || window.documentElement.scrollTop || document.body.scrollTop;
      console.log(scrollTop)
     if(scrollTop > 300 && scrollTop < 900){
        this.showIntro = true
      }else  if(scrollTop > 900 && scrollTop < 1600){
        this.showPic = true
      } else  if(scrollTop > 1600 && scrollTop < 2000){
        this.showNews = true
      }else if(scrollTop >2000){
       this.showCont = true
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
