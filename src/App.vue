<template>
  <div id="app">
    <router-view/>
    <!-- <div id="jsi-flying-fish-container" class="footer-fish-container"></div> -->
  </div>
</template>

<script>
export default {
  name: 'App',
  created () {
    // love2d看板娘
    window.L2Dwidget.init({
      // 更换模型地址前后都需要修改
      // 示例:'https://unpkg.com/live2d-widget-model-unitychan/assets/unitychan.model.json'
      model: {
        jsonPath: 'https://unpkg.com/live2d-widget-model-hijiki/assets/hijiki.model.json',
        scale: 1
      },
      // 设置位置
      display: {
        position: 'left',
        width: 100,
        height: 180,
        hOffset: 70,
        vOffset: 0
      },
      // 手机设置
      mobile: {
        show: true,
        scale: 0.5
      },
      // 透明度设置
      react: {
        opacityDefault: 1,
        opacityOnHover: 1
      }
    })
  }
}
</script>

<style lang="less" scoped>
#app {
  // &::after{
  //   content: "";
  //   position: fixed;
  //   top: 0;
  //   left: 0;
  //   width: 100%;
  //   height: 100%;
  //   z-index: -1;
  //   background-repeat: no-repeat;
  //   background-position: center;
  //   background-size: cover;
  //   background-image: url(https://api.imacroc.cn/acg/);
  //   opacity: 0.06;
  //   -webkit-filter: grayscale(100%);
  //   -moz-filter: grayscale(100%);
  //   -ms-filter: grayscale(100%);
  //   -o-filter: grayscale(100%);
  //   filter: grayscale(100%);
  //   filter: gray;
  // }

  .footer-fish-container {
    position: fixed;
    bottom: -60px;
    left: 0;
    z-index: 99;
    width: 100%;
    pointer-events: none;
  }
}
</style>
