<template>
    <div class="contact">
      <transition name="move">
        <div class="menu" v-show="msg">
          <div class="contact-border">
            <div class="contact-first">
          <p class="contact-first-1">联系我们</p>
          <p><img src="../images/line.png" /></p>
        </div>
            <div class="contact-sec">
          <p class="contact-sec-1">告诉我们您想要的吧</p>
          <div class="contact-sec-2"><span><img src="../images/phone.png" /></span> 020-00000000</div>
        </div>
            <div class="contact-thir">
          <p>&copy;2018-版权所有</p>
          <p>手机版|本站使用凡科建站 搭建|管理登录</p>
        </div>
          </div>
        </div>
      </transition>
    </div>
</template>

<script>
    export default {
        name: "Contact",
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
.contact{
  position: absolute;
  top: 2660px;
  height: 261px;
  width: 100%;
  background-color: #222222;
}
  .contact-border{
    width: 1200px;
    margin: 0 auto;
    position: relative;
    top: 15px;
  }

  .contact-first-1{
    color: rgb(255,255,255);
    font-size: 28px;
    margin-bottom: 10px;
    margin-top: 15px;
  }
  .contact-sec-1{
    font-size: 13px;
    color: rgb(222, 222, 222);
    margin-bottom: 10px;
    margin-top: 20px;
  }
  .contact-sec-2{
    font-size: 25px;
    color: rgb(255,255,255);
    margin-bottom: 10px;
  }
  .contact-sec-2 span{
    position: relative;
    top: 5px;
  }
  .contact-thir{
    font-size: 12px;
    color: #9b9b9b;
    font-family: 微软雅黑;
    margin-top: 25px;
  }
  .contact-thir p{
    margin-top: 5px;
  }
.menu{
  display: inline-block;
  transition:all 0.7s linear;
}
/*上面主要都是样式代码*/
.move-enter-active > .contact-border{
  animation: animation  2s ease-in;
}

@keyframes animation {
  0%{transform: rotateY(0deg)}
  25%{
    -webkit-transform: rotateY(90deg);
    -moz-transform: rotateY(90deg);
    -ms-transform: rotateY(90deg);
    -o-transform: rotateY(90deg);
    transform: rotateY(90deg);
  }
  50%{
    -webkit-transform: rotateY(180deg);
    -moz-transform: rotateY(180deg);
    -ms-transform: rotateY(180deg);
    -o-transform: rotateY(180deg);
    transform: rotateY(180deg);}
  75%{
    -webkit-transform: rotateY(270deg);
    -moz-transform: rotateY(270deg);
    -ms-transform: rotateY(270deg);
    -o-transform: rotateY(270deg);
    transform: rotateY(270deg);
  }
  100%{
    -webkit-transform: rotateY(360deg);
    -moz-transform: rotateY(360deg);
    -ms-transform: rotateY(360deg);
    -o-transform: rotateY(360deg);
    transform: rotateY(360deg);
  }
}
</style>
