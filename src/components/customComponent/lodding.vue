<template>
  <div class="load-container" v-show="show">
    <div class="load-mask" :style="{'opacity':opacitys}" v-show="isShowMask">
    </div>
    <div class="circle-wrapper">
      <div class="circle_1 circle" :style="{'background-color': color}"></div>
      <div class="circle_2 circle" :style="{'background-color': color}"></div>
      <div class="circle_3 circle" :style="{'background-color': color}"></div>
      <div class="circle_4 circle" :style="{'background-color': color}"></div>
      <div class="circle_5 circle" :style="{'background-color': color}"></div>
      <div class="circle_6 circle" :style="{'background-color': color}"></div>
      <div class="circle_7 circle" :style="{'background-color': color}"></div>
      <div class="circle_8 circle" :style="{'background-color': color}"></div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "lodding",
    props: {
      show: {
        default: false,
        type: Boolean
      },
      color:{
        default:'#50B4B6'
      },
      isShowMask: {
        type: Boolean,
        default: false
      },
      opacitys:{
        type:Number,
        default:1
      }
    }
  }
</script>

<style scoped>
  .load-container {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    overflow: hidden;
    box-sizing: border-box;
  }
  .load-mask {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    opacity: 0.5;
    background-color: #fff;
    z-index: 99;
  }
  .circle-wrapper {
    position: absolute;
    top: 50%;
    left: 50%;
    -webkit-transform: translate(-50%, -50%);
    transform: translate(-50%, -50%);
    width: 58px;
    height: 58px;
    z-index: 9999;
  }

  .circle {
    position: absolute;
    /*background-color: #50B4B6;*/
    width: 14px;
    height: 14px;
    border-radius: 9px;
    -webkit-animation-name: bounce_circular;
    animation-name: bounce_circular;
    -webkit-animation-duration: 1.1s;
    animation-duration: 1.1s;
    -webkit-animation-iteration-count: infinite;
    animation-iteration-count: infinite;
    -webkit-animation-direction: normal;
    animation-direction: normal;
  }

  .circle_1 {
    left: 0;
    top: 23px;
    -webkit-animation-delay: 0.41s;
    animation-delay: 0.41s;
  }

  .circle_2 {
    left: 6px;
    top: 6px;
    -webkit-animation-delay: 0.55s;
    animation-delay: 0.55s;
  }

  .circle_3 {
    top: 0;
    left: 23px;
    -webkit-animation-delay: 0.69s;
    animation-delay: 0.69s;
  }

  .circle_4 {
    right: 6px;
    top: 6px;
    -webkit-animation-delay: 0.83s;
    animation-delay: 0.83s;
  }

  .circle_5 {
    right: 0;
    top: 23px;
    -webkit-animation-delay: 0.97s;
    animation-delay: 0.97s;
  }

  .circle_6 {
    right: 6px;
    bottom: 6px;
    -webkit-animation-delay: 1.1s;
    animation-delay: 1.1s;
  }

  .circle_7 {
    left: 23px;
    bottom: 0;
    -webkit-animation-delay: 1.24s;
    animation-delay: 1.24s;
  }

  .circle_8 {
    left: 6px;
    bottom: 6px;
    -webkit-animation-delay: 1.38s;
    animation-delay: 1.38s;
  }

  @keyframes bounce_circular {
    0% {
      -webkit-transform: scale(1);
      transform: scale(1);
    }

    100% {
      -webkit-transform: scale(0.3);
      transform: scale(0.3);
    }
  }
</style>
