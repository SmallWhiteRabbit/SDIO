<template>
  <div class="" style="margin: 0 auto;width: 100%">
    <div class="nav-top">
      <p class="name">
        <span class="electronics">Electronics </span>Design
      </p>
      <ul class="nav" >
        <li class="active"><a href="" >首页</a> </li>
        <li><a href="">产品展示</a> </li>
        <li><a href="">行业动态</a> </li>
        <li><a href="">关于我们</a> </li>
        <li><a href="">联系我们</a> </li>
      </ul>
      <div style="clear: left"></div>
    </div>
    <div class="nav-pic">
      <div class="nav-word">
        <div class="nav-words">
          <span class="nav-word-elec">电子电工</span>
          <p class="nav-word-cont" >12年坚持捍卫民族电工精工品质，千万次重复，品质始终如一，从模具到材料加工，从不见到成品组装176道工序，68个质控点...</p>

        </div>
           </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >

  .nav-top{
    min-width: 1200px;
    width: 100%;
    height: 120px;
    margin: 0 auto;
    position: relative;

  }
  .name{
    font-weight: bold;
    color: rgb(204,204,204);
    font-size: 32px;
    display: inline-block;
    line-height: 120px;
    position: relative;
    right: 50px;
  }
  .electronics{
    color: rgb(255,192,1);
  }
  .nav{
    list-style: none;
    display: inline-block;
    position: relative;
    top: 12px;
    left: 75px;
  }
  .nav li{
    float: left;
    width: 100px;
    height: 50px;
    line-height: 50px;
    margin: 0px 9px;
  }
  .nav li a{
    color: black;text-decoration: none;font-size: 20px;
  }
  .nav li:hover,.active{
    background-color: rgb(255,192,1);
    border-radius: 30%;

  }

  .active a{ color: white!important;}
  .nav li:hover a{color: white;}
  .nav-pic{
    width: 100%;
    height: 500px;
    background-image: url("../images/head.jpg");
    background-size: cover;
    background-position-x: -300px;
  }
  .nav-word{
    min-width: 1200px;
    height: 500px;
    margin: 0 auto;
  }
  .nav-words{
    position: relative;
    margin-left: 730px;
    padding-top: 80px;
    text-align: left;

  }
  .nav-word-elec{
    font-size: 49px;
    color: rgb(255,255,255);
  }
  .nav-word-cont{
    width: 435px;
    height: 87px;
    min-height: 40px;
    position: relative;
    top: 10px;
    color: rgb(255,255,255);
    font-size: 18px;
    line-height: 28px;

  }
  </style>
