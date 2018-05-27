<template>
    <div class="picture-back">
      <transition name="move">
        <div class="menu" v-show="msg">
          <div class="picture-pos">
            <div class="picture-block">
              <span class="picture-show"><img src="../images/pic1-1.png"/></span>
              <span class="picture-hid"><img src="../images/pic1-2.jpg"/></span>
            </div>
            <div class="picture-block">
          <span class="picture-show"><img src="../images/pic2-2.jpg" /></span>
          <span  class="picture-hid"><img src="../images/pic2-1.jpg" /></span>
        </div>
            <div class="picture-block">
          <span class="picture-show"><img src="../images/pic3-1.jpg"></span>
          <span  class="picture-hid"><img src="../images/pic3-2.jpg"></span>
        </div>
            <div class="picture-block">
          <span class="picture-show"><img src="../images/pic4-2.png" /></span>
          <span  class="picture-hid"><img src="../images/pic4-1.jpg" /></span>
        </div>
            <div class="picture-block">
          <span class="picture-show"><img src="../images/pic5-1.jpg"/></span>
          <span  class="picture-hid"><img src="../images/pic5-2.jpg"/></span>
        </div>
            <div class="picture-block">
          <span class="picture-show"><img src="../images/pic6-2.jpg"/></span>
          <span  class="picture-hid"><img src="../images/pic6-1.jpg"/></span>
        </div>
          </div>
        </div>
      </transition>
    </div>
</template>

<script>
    export default {
        name: "Picture",
      data() {
        return {
          show: false
        };
      },
      props:{
          msg:Boolean
      },
    }
</script>

<style scoped>
.picture-back{
  height: 778px;
  position: absolute;
  top: 1315px;
  width: 100%;
  background-color: #f5f5f5; margin: 0 auto;
}
  .picture-pos{
    width: 1210px;
    margin: 0 auto;
    position: relative;top: 13%;
  }
  .picture-block{
    display: inline-block;
    width: 400px;
    height: 280px;
  }
  .picture-hid{
    display: none;
  }

  .picture-block:hover .picture-hid{
    display: inline-block;
    /*position: relative;top: 0px;left: 0px;*/
  }
  .picture-block:hover .picture-show{
  display: none;
}
.menu{
  display: inline-block;   width: 1210px;
  margin: 0 auto;    position: relative;top: 13%;
  transition:all 0.7s linear;
}
/*上面主要都是样式代码*/
.move-enter-active > .picture-pos{
  animation: animation  2s ease-in-out;
}

@keyframes animation {
  0%{transform: scale(0) }
  50%{-webkit-transform: scale(0.5);
    -moz-transform: scale(0.5) ;
    -ms-transform: scale(0.5);
    -o-transform: scale(0.5) ;
    transform: scale(0.5) }
  75%{-webkit-transform: scale(0.75);
    -moz-transform: scale(0.75) ;
    -ms-transform: scale(0.75) ;
    -o-transform: scale(0.75) ;
    transform: scale(0.75) ;}
  100%{
    -webkit-transform: scale(1) ;
    -moz-transform: scale(1) ;
    -ms-transform: scale(1) ;
    -o-transform: scale(1) ;
    transform: scale(1) ;}
}
</style>
