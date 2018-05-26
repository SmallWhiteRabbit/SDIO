<template>
    <div class="picture-back">
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
</template>

<script>
    export default {
        name: "Picture"
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
</style>
