<template>
    <div class="news">
      <div class="new-border">
        <transition name="move">
          <div class="menu" v-show="msg">
            <div class="new-tittle">
              <p>新闻动态</p>
              <p class="new-tittle-cha">NEWS</p>
            </div>
          </div>
        </transition>
        <transition name="move">
          <div class="menu" v-show="msg">
            <div class="new-cont">
          <div class="new-cont-date"><span class="new-cont-day">24</span><span class="new-cont-year">2018/05</span></div>
          <div class="new-cont-cont">
            <p class="new-cont-cont-tittle">美国研究人员发现树叶也可做电池</p>
            <span class="new-cont-cont-intro">树叶也能做电池？对，你没有看错。美国马里兰大学的研究人员用树叶和一</span>
          </div>
        </div>
            <div class="new-cont">
          <div class="new-cont-date"><span class="new-cont-day">24</span><span  class="new-cont-year">2018/05</span></div>
          <div class="new-cont-cont">
            <p>智能家具互联、互通 尚需五年</p>
            <span>物联网时代是如此诱人，作为物联网时代的最重要的组成部分之一，智能家居的</span>
          </div>
        </div>
            <div class="new-cont">
          <div class="new-cont-date"><span class="new-cont-day">24</span><span  class="new-cont-year">2018/05</span></div>
          <div class="new-cont-cont">
            <p>冬季用电紧张 当空调遭遇电压不稳咋办？</p>
            <span>在冬季用电高峰期，电压不稳的情况可能会在一定的情况下出现，这时候，就是得</span>
          </div>
        </div>
            <div class="new-cont">
          <div class="new-cont-date"><span class="new-cont-day">24</span><span  class="new-cont-year">2018/05</span></div>
          <div class="new-cont-cont">
            <p >CPU烧到宕机 散热器这么使用你就傻了</p>
            <span>不少DIY玩家在攒机时对硬件的选额慎而又慎，让不同硬件的搭配可以发挥</span>
          </div>
        </div>
          </div>
        </transition>
      </div>

    </div>
</template>

<script>
    export default {
        name: "News",
      data() {
        return {
          show: false
        };
      },
      props:{
        msg:Boolean
      }
    }
</script>

<style scoped>
.news{
  position: absolute;
  top:2093px ;
  height: 507px;
  margin: 0 auto;
  width: 100%;
}
  .new-border{
    width: 1200px;
    margin: 0 auto;
    padding: 80px 0px 80px;
  }
  .new-tittle{
    font-size: 32px;
    line-height: 40px;
  }
  .new-tittle-cha {
    font-size: 22px;
    height: 40px;
    line-height: 50px;
  }
  .new-cont{
    display: inline-block;
    width:  48%;
    margin-top: 30px;
  }
  .new-cont-date{
    width: 80px;
    height: 80px;
    background-color: #f2f2f2;
    display: inline-block;
    position: relative;
    top: 12px;
    color: #808080;
  }
  .new-cont-day{
    font-size: 25px;
    line-height: 25px;
    font-family: "微软雅黑 Light";
    display: inline-block;
    position: relative;
    top: 17px;
  }
  .new-cont-year{
    font-size: 14px;
    line-height: 14px;
    display: block;
    position: relative;
    top: 15px;
  }
  .new-cont-cont{
    display: inline-block;
    width: 380px;
    height: 80px;
    position: relative;
    top: 35px;
    left: 5px;
    text-align: left;
    color: #808080;
  }
.new-cont-cont-tittle{
  font-size: 18px;
  font-family: 微软雅黑;
  position: relative;
  top: 5px;
}
  .new-cont-cont-intro{
    display: inline-block;
    font-size: 14px;
    width: 253px;
    font-family: 微软雅黑;
    position: relative;
    top: 10px;
  }

.menu{
  display: inline-block;
  transition:all 0.7s linear;
}
/*上面主要都是样式代码*/
.move-enter-active > .new-cont,.new-tittle{
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
