<template>
  <div class="mm-shopping">
    <div class="mm-shopping__hd">
      <h2>手机</h2>
      <div class="shopping-hd__more">
        <a href="">查看更多</a>
        <i class="iconfont iconfont-arrow-right-big"></i>
      </div>
    </div>

    <div class="mm-shopping__thumb">
      <a href="">
        <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/c583f2edc613f1be20fa415910b13ce3.jpg?thumb=1&w=234&h=614&f=webp&q=90" alt="">
      </a>
    </div>
    <div class="mm-shopping__item">
      <a v-for="(shoppingItem, index) in shoppingItems" :key="index" href="">
        <div class="shopping-item__content">
          <img :src="shoppingItem.src" alt="">
          <h3>{{ shoppingItem.title }}</h3>
          <p class="content-desc">{{ shoppingItem.desc }}</p>
          <p class="content-price">
            <span>{{ shoppingItem.price.cur }}</span>元起
            <del>{{ shoppingItem.price.del }}元</del>
          </p>
        </div>
      </a>
    </div>
    <img class="shopping-img" src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/41d16e66381cfeda7b6b39ab67678d5e.jpg?thumb=1&w=1533&h=150&f=webp&q=90" alt="">
  </div>
</template>

<script>
import { reactive } from '@vue/reactivity'
export default {
  name: 'MiPhone',
  setup() {
    const shoppingItems = reactive([
      {
        src: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/61454401f855cf5ed64747a6ac04bae5.jpg?thumb=1&w=200&h=200&f=webp&q=90',
        title: 'Note 10 Pro',
        desc: '天玑1100年度旗舰芯，VC液冷散热',
        price: {
          cur: '1599',
          del: '1699'
        }
      },
      {
        src: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/20d36fbaa18625e4fe507af31e4e9f83.jpg?thumb=1&w=250&h=250&f=webp&q=90',
        title: '全面屏电视E43K',
        desc: '全面屏设计，海量内容',
        price: {
          cur: '1399',
          del: '1599'
        }
      },
      {
        src: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/20d36fbaa18625e4fe507af31e4e9f83.jpg?thumb=1&w=250&h=250&f=webp&q=90',
        title: '全面屏电视E43K',
        desc: '全面屏设计，海量内容',
        price: {
          cur: '1399',
          del: '1599'
        }
      },
      {
        src: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/20d36fbaa18625e4fe507af31e4e9f83.jpg?thumb=1&w=250&h=250&f=webp&q=90',
        title: '全面屏电视E43K',
        desc: '全面屏设计，海量内容',
        price: {
          cur: '1399',
          del: '1599'
        }
      },
      {
        src: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/20d36fbaa18625e4fe507af31e4e9f83.jpg?thumb=1&w=250&h=250&f=webp&q=90',
        title: '全面屏电视E43K',
        desc: '全面屏设计，海量内容',
        price: {
          cur: '1399',
          del: '1599'
        }
      },
      {
        src: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/20d36fbaa18625e4fe507af31e4e9f83.jpg?thumb=1&w=250&h=250&f=webp&q=90',
        title: '全面屏电视E43K',
        desc: '全面屏设计，海量内容',
        price: {
          cur: '1399',
          del: '1599'
        }
      },
      {
        src: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/20d36fbaa18625e4fe507af31e4e9f83.jpg?thumb=1&w=250&h=250&f=webp&q=90',
        title: '全面屏电视E43K',
        desc: '全面屏设计，海量内容',
        price: {
          cur: '1399',
          del: '1599'
        }
      },
      {
        src: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/20d36fbaa18625e4fe507af31e4e9f83.jpg?thumb=1&w=250&h=250&f=webp&q=90',
        title: '全面屏电视E43K',
        desc: '全面屏设计，海量内容',
        price: {
          cur: '1399',
          del: '1599'
        }
      },
    ])

    return { shoppingItems }
  }
}
</script>

<style lang='scss' scoped>
.mm-shopping {
  margin-bottom: 22px;
}

.mm-shopping img {
  width: 1226px;
  height: 120px;
}

.mm-shopping__hd {
  position: relative;
  height: 58px;
}

.shopping-hd__more {
  position: absolute;
  right: 0;
  top: 0;
  &:hover {
    & a {
      color: #ff6700;
    }
    & i {
      background-color: #ff6700;
    }
  }
  & a {
    font-size: 16px;
    line-height: 58px;
    color: #424242;
    -webkit-transition: all .4s;
    transition: all .4s;
  }
  & i {
    width: 12px;
    height: 12px;
    padding: 4px;
    margin-left: 8px;
    border-radius: 16px;
    font-size: 12px;
    line-height: 12px;
    background: #b0b0b0;
    color: #fff;
    vertical-align: 1px;
    -webkit-transition: all .4s;
    transition: all .4s;
  }
}

.hd-more__active {
  color: #ff6700;
  border-bottom: 2px solid #ff6700;
}

.mm-shopping__thumb {
  float: left;
  width: 234px;
}

.mm-shopping__thumb li { 
  background-color: #fff;
  height: 300px;
  width: 234px;
  margin-bottom: 14px;
}

.mm-shopping__thumb img {
  width: 234px;
  height: 614px;
  transition: all .2s linear;
  &:hover {
    z-index: 2;
    -webkit-box-shadow: 0 15px 30px rgb(0 0 0 / 10%);
    box-shadow: 0 15px 30px rgb(0 0 0 / 10%);
    -webkit-transform: translate3d(0,-2px,0);
    transform: translate3d(0,-2px,0);
  }
}

.mm-shopping__item {
  display: grid;
  grid-template-rows: repeat(2, 1fr);
  grid-template-columns: repeat(4, 1fr);
  grid-row-gap: 13px;
}

.mm-shopping .mm-shopping__item a {
  display: inline-block;
  background-color: #fff;
  width: 234px;
  height: 300px;
  text-align: center;
  padding: 20px;
  margin-left: calc(56px / 4);
  flex-grow:0;
  flex-shrink:0;
  transition: all .2s linear;
  &:hover {
    z-index: 2;
    -webkit-box-shadow: 0 15px 30px rgb(0 0 0 / 10%);
    box-shadow: 0 15px 30px rgb(0 0 0 / 10%);
    -webkit-transform: translate3d(0,-2px,0);
    transform: translate3d(0,-2px,0);
  }
}

.mm-shopping .mm-shopping__item .shopping-item__content img {
  margin: 0;
  width: 160px;
  height: 160px;
  margin-bottom: 12px;
}

.mm-shopping .mm-shopping__item .shopping-item__content h3 {
  margin: 0 20px 2px;
  font-size: 14px;
  font-weight: 400;
  text-overflow: ellipsis;
  color: #212121;
  overflow: hidden;
  white-space: nowrap;
}

.mm-shopping .mm-shopping__item .shopping-item__content .content-desc {
  height: 18px;
  margin: 0 10px 10px;
  font-size: 12px;
  text-overflow: ellipsis;
  color: #b0b0b0;
  overflow: hidden;
  white-space: nowrap;
  margin-bottom: 12px;
}

.mm-shopping .mm-shopping__item .shopping-item__content .content-price {
  margin: 0;
  color: #ff6709;
  font-size: 14px;
}

.shopping-img {
  margin: 22px 0;
}
</style>