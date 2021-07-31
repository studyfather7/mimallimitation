<template>
  <div class="mi-header">
    <div class="wrapper">
      <div class="mi-header__logo">
        <a href="">
          <img src="../assets/img/logo-mi2.png" alt="">
        </a>
      </div>
      <div class="mi-header__ct">
        <ul>
          <li v-for="(navItem, index) in navItems" :key="index">
            <a href="">
              <span>{{ navItem }}</span>
            </a>
          </li>
        </ul>
      </div>
      <div class="mi-header__search">
        <input :class="{ active: show == 1 }" @focus="show = 1" @blur="show = 0" type="search" class="mi-header__search--input">
        <input :class="{ active: show == 1 }" type="submit" value="" class="mi-header__search--btn iconfont">
      </div>
    </div>
  </div>
</template>

<script>
import { reactive, ref } from '@vue/reactivity'
export default {
  name: 'MiHeader',
  setup() {
    let show = ref(0);
    const navItems = reactive([
      '小米手机',
      'Redmi 红米',
      '电视',
      '笔记本',
      '家电',
      '路由器',
      '智能硬件',
      '服务',
      '社区',
    ])
    return { navItems, show }
  }
}
</script>

<style lang='scss'>
.mi-header {
  position: relative;
  height: 100px;
  z-index: 20;
  &__logo {
    float: left;
    margin-top: 22px;
    & a img {
      width: 56px;
      height: 56px;
    }
  }
  &__ct {
    float: left;
    width: 850px;
    & ul {
      position: relative;
      float: left;
      width: 1100px;
      height: 88px;
      margin: 0;
      padding: 12px 0 0 178px;
      list-style-type: none;
      font-size: 16px;
      &  li {
        float: left;        
        & a {
          text-decoration: none;
          display: block;
          padding: 26px 10px 38px;
          color: #333;
          -webkit-transition: color .2s;
          transition: color .2s;
          & span {
            color: #333;
            &:hover {
              color: #ff6700;
            }
          }
        }
      }
    }
  }
  &__search {
    position: relative;
    float: right;
    width: 296px;
    margin-top: 25px;
    &:hover input {
      border: 1px solid #b0b0b0;
    }
    & input.active {
      border: 1px solid #ff6700;
    } 
    &--input {
      position: absolute;
      top: 0;
      border: 1px solid #e0e0e0;
      outline: 0;
      -webkit-transition: all .2s;
      transition: all .2s;
      right: 51px;
      z-index: 1;
      width: 223px;
      height: 48px;
      padding: 0 10px;
      font-size: 14px;
      line-height: 48px;
      -webkit-appearance: textfield;
      -webkit-box-sizing: content-box;
      box-sizing: content-box;
    }
    &--btn {
      right: 0;
      z-index: 2;
      width: 52px;
      height: 50px;
      font-size: 24px;
      line-height: 24px;
      background: #fff;
      color: #616161;
      position: absolute;
      top: 0;
      border: 1px solid #e0e0e0;
      outline: 0;
      -webkit-transition: all .2s;
      transition: all .2s;
    }
  }
}
</style>