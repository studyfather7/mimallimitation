<template>
  <div class="mi-topbar">
    <div class="wrapper">
      <div class="mi-topbar__lt">
        <template v-for="(menuItem, index) in menuItems" :key="index"> 
          <a href="">{{ menuItem }}</a>
          <span v-if="index != menuItems.length - 1">|</span>
        </template>
      </div>

      <div class="mi-topbar__cart">
        <a 
          @mouseover="drop()" 
          @mouseout="raise()"
          href="">
          <em class="iconfont-cart"></em>
          购物车（0）
        </a>
        <div 
          @mouseover="cartH = 100" 
          @mouseout="cartH = 0"
          class="mi-topbar__cart--drop drop" :style="{ height: cartH + 'px' }">
          <div class="drop-menu">
            <div class="loading" v-show="show == 1">
              <div class="loader"></div>
            </div>
            <div class="drop-menu-msg"><p v-show="show == 0">购物车中还没有商品，赶紧选购吧！</p></div>
          </div>
        </div>
      </div>

      <div class="mi-topbar__rt">
        <template v-for="(userItem, index) in userItems" :key="index">
          <a href="">{{ userItem }}</a>
          <span v-if="index != userItems.length - 1">|</span>
        </template>
      </div>
    </div>
  </div>
</template>

<script>
import { reactive, ref } from '@vue/reactivity'
export default {
  name: 'MiTopbar',
  setup() {
    const menuItems = reactive([
      '小米商城',
      'MIUI',
      'IoT',
      '云服务',
      '天星数科',
      '有品',
      '小爱开放平台',
      '企业团购',
      '资质证照',
      '协议规则',
      '下载app',
      '智能生活',
      'Select Location'
    ])

    const userItems = reactive([
      '登录',
      '注册',
      '消息通知',
    ])
    
    let cartH = ref(0)
    let show = ref(1)
    function drop() {
      cartH.value = 100
      setTimeout(() => {
        show.value = 0
      }, 1500)
    }

    function raise() {
      cartH.value = 0
      show.value = 1;
    }

    return { menuItems, userItems, cartH, show, drop, raise }
  }
}
</script>

<style lang='scss'>
.mi-topbar {
  position: relative;
  height: 40px;
  font-size: 12px;
  color: #b0b0b0;
  background: #333;
  z-index: 30;
  &__lt {
    float: left;
  }
  &__rt {
    float: right;
  }
  & a {
    text-decoration: none;
    color: #b0b0b0;
    line-height: 40px;
    display: inline-block;
    &:hover {
      color: #fff;
    }
  }
  & span {
    margin: 0 .3em;
    color: #424242;
  }
  &__cart {
    position: relative;
    float: right;
    width: 120px;
    height: 40px;
    margin-left: 15px;
    -webkit-transition: all .2s;
    transition: all .2s;
    font-size: 12px;
    & a {
      position: relative;
      display: block;
      height: 40px;
      line-height: 40px;
      text-align: center;
      color: #b0b0b0;
      background: #424242;
      &:hover {
        color: #ff6700;
        background: #fff;
      }
    }
    & em {
      margin-right: 4px;
      font-size: 20px;
      line-height: 20px;
      vertical-align: -4px;
    }
    &--drop {
      position: absolute;
      right: 0;
      top: 40px;
      width: 316px;
      height: 0;
      color: #424242;
      background: #fff;
      -webkit-box-shadow: 0 2px 10px rgb(0 0 0 / 15%);
      box-shadow: 0 2px 10px rgb(0 0 0 / 15%);
      overflow: hidden;
      -webkit-transition: height .3s;
      transition: height .3s;
    }
  }
}

.loading {
  margin: 0 20px 20px;
  text-align: center;
  padding: 20px 0;
  .loader {
    position: relative;
    margin: 0 auto;
    width: 4px;
    height: 20px;
    background: #ff6700;
    overflow: visible;
    -webkit-animation-delay: 0s;
    animation-delay: 0s;
    -webkit-transform: scale(1);
    -ms-transform: scale(1);
    transform: scale(1);
  }
  .loader, .loader:after, .loader:before {
    -webkit-transform-origin: 50% 50%;
    -ms-transform-origin: 50% 50%;
    transform-origin: 50% 50%;
    -webkit-animation-name: loader;
    animation-name: loader;
    -webkit-animation-duration: .3s;
    animation-duration: .3s;
    -webkit-animation-timing-function: linear;
    animation-timing-function: linear;
    -webkit-animation-iteration-count: infinite;
    animation-iteration-count: infinite;
    animation-direction: alternate-reverse;
  }
}


.loader:before {
  margin: -10px 0 0 -10px;
  -webkit-animation-delay: .25s;
  animation-delay: .25s;
  -webkit-transform: scaleY(.3);
  -ms-transform: scaleY(.3);
  transform: scaleY(.3);
}

.loader:after, .loader:before {
    position: absolute;
    left: 50%;
    top: 50%;
    width: 4px;
    height: 20px;
    content: "";
    background: #ff6700;
}

.loader, .loader:after, .loader:before {
    -webkit-transform-origin: 50% 50%;
    -ms-transform-origin: 50% 50%;
    transform-origin: 50% 50%;
    -webkit-animation-name: loader;
    animation-name: loader;
    -webkit-animation-duration: .3s;
    animation-duration: .3s;
    -webkit-animation-timing-function: linear;
    animation-timing-function: linear;
    -webkit-animation-iteration-count: infinite;
    animation-iteration-count: infinite;
    animation-direction: alternate-reverse;
}

.loader:after {
    margin: -10px 0 0 6px;
    -webkit-animation-delay: .5s;
    animation-delay: .5s;
    -webkit-transform: scaleY(.5);
    -ms-transform: scaleY(.5);
    transform: scaleY(.5);
}

.loader:after, .loader:before {
    position: absolute;
    left: 50%;
    top: 50%;
    width: 4px;
    height: 20px;
    content: "";
    background: #ff6700;
}

.loader, .loader:after, .loader:before {
    -webkit-transform-origin: 50% 50%;
    -ms-transform-origin: 50% 50%;
    transform-origin: 50% 50%;
    -webkit-animation-name: loader;
    animation-name: loader;
    -webkit-animation-duration: .3s;
    animation-duration: .3s;
    -webkit-animation-timing-function: linear;
    animation-timing-function: linear;
    -webkit-animation-iteration-count: infinite;
    animation-iteration-count: infinite;
    animation-direction: alternate-reverse;
}
@keyframes loader {
  0% {
      -webkit-transform: scaleY(.5);
      transform: scaleY(.5);
      opacity: .2;
  }
  100% {
      -webkit-transform: scale(1);
      transform: scale(1);
      opacity: 1;
  }
}

.drop {
  &-menu {
    padding-top: 20px;
    &-msg {
      text-align: center;
      padding-top: 20px;
    }
  }
}
</style>