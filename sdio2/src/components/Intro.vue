<template>
  <div class="intro">
    <div class="intro-border"  >
      <transition name="move">
        <div class="menu" v-show="msg">
          <div class="safe intro-cont">
            <div class="intro-pos">
              <p><img src="../images/safe.png" /></p>
              <p class="intro-tittle">安全高品质</p>
              <p>12年坚持捍卫民族电工精工品质</p>
              <p>千万次重复，品质始终如一</p>
              <p>从 模具到材料加工，从不见到成品组装</p>
              <p>176道工序，68个质控点</p>
            </div>
          </div>
        </div>
      </transition>
      <transition name="move">
        <div class="menu" v-show="msg">
          <div class="major intro-cont">
        <div class="intro-pos">
          <p><img src="../images/major.png" /></p>
          <p class="intro-tittle">专业设计团队</p>
          <p>我们有专业的优秀设计师</p>
          <p>我们不断的从变革创新到超越</p>
          <p>使我们的商品更好用，更方便，更安全</p>
          <p>因为您的选择让我们更有动力</p>
        </div>
      </div>
        </div>
      </transition>
      <transition name="move">
        <div class="menu" v-show="msg">
          <div class="sale intro-cont">
            <div class="intro-pos">
          <p><img src="../images/sale.png" /></p>
          <p class="intro-tittle">贴心售后</p>
          <p>专业贴心的售后团队，让你售后无忧</p>
          <p>我们朝着安全环保的方向发展</p>
          <p>悉心为您的打造休闲现代生活</p>
          <p>贴心服务，强大的售后团队支持</p>
        </div>
          </div>
        </div>
      </transition>
    </div>
  </div>

</template>

<script>
    export default {
        name: "Intro",
      data() {
        return {
          show: false,
        };
      },
      props:{
          msg:Boolean
      }

    }
</script>

<style scoped>
.intro{
  width: 100%;
  height: 695px;
  position: absolute;
  top: 620px;
}

.intro-border{
  width: 1222px;
  margin: 0 auto;
  display: inline-block;
  padding-top: 130px;
}
  .intro-cont{
    display: inline-block;
    width: 404px;
    height: 467px;
    position: relative;
    top: 15%;
    background-size: cover;
  }

.safe{
  background-image: url("../images/border2.png");
  left: 20px;
  z-index: 2;
}
.major{
  background-image: url("../images/border1.png");
  z-index: 1;
}
.sale{
  background-image: url("../images/border3.png");
  right: 20px;
  z-index: 2;
}
.intro-pos{
  position: relative;
  top: 100px;
}
.intro-pos p:not(.intro-tittle){
  color: rgb(153,153,153);
  font-size: 14px;
}
.intro-tittle{
  color: rgb(51, 51, 51);
  font-size: 20px;
  font-family: 微软雅黑;
  margin-top: 20px;
  margin-bottom: 40px;
}
.menu{display: inline-block;
  transition:all 0.7s linear;}
.move-enter-active > .intro-cont{
  animation: animation  2s ease-in-out;
}

@keyframes animation {
  0%{transform: scale(0) rotate(0deg)}
  50%{-webkit-transform: scale(0.5) rotate(180deg);
    -moz-transform: scale(0.5) rotate(180deg);
    -ms-transform: scale(0.5) rotate(180deg);
    -o-transform: scale(0.5) rotate(180deg);
    transform: scale(0.5) rotate(180deg);}
  75%{-webkit-transform: scale(0.75) rotate(270deg);
    -moz-transform: scale(0.75) rotate(270deg);
    -ms-transform: scale(0.75) rotate(270deg);
    -o-transform: scale(0.75) rotate(270deg);
    transform: scale(0.75) rotate(270deg);}
  100%{
    -webkit-transform: scale(1) rotate(360deg);
    -moz-transform: scale(1) rotate(360deg);
    -ms-transform: scale(1) rotate(360deg);
    -o-transform: scale(1) rotate(360deg);
    transform: scale(1) rotate(360deg);}
}

</style>
