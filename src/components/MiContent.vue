<template>
  <div class="content">
    <div class="wrapper">
      <mi-seckill/>
      <mi-phone/>
      <mi-shopping 
        v-for="(shopping, index) in shoppings" :key="index"
        :title="shopping.title" 
        :list="shopping.moreList" 
        :items="shopping.shoppingItems" 
        :img="shopping.img"
        :thumb="shopping.shoppingThumb"/>
      <mi-vedio/>
    </div>
  </div>
</template>

<script>
import MiSeckill from './MiSeckill.vue'
import MiPhone from './MiPhone.vue'
import MiShopping from './MiShopping.vue'
import MiVedio from './MiVedio.vue'
import { reactive } from '@vue/reactivity'
export default {
  name: 'MiContent',
  components: { MiSeckill, MiShopping, MiPhone, MiVedio },
  setup() {
    const shoppings = reactive([
      {
        title: '家电',
        img: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/41d16e66381cfeda7b6b39ab67678d5e.jpg?thumb=1&w=1533&h=150&f=webp&q=90',
        moreList: [
          '热门',
          '电影影音'
        ],
        shoppingThumb: [
          'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/116fc43816b87192be4e67cf762e8da5.jpeg?thumb=1&w=293&h=375&f=webp&q=90',
          'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/dfbdabe36b2d630d57a015e6fb5eb3ea.jpg?thumb=1&w=293&h=375&f=webp&q=90'
        ],
        shoppingItems: [
          [
            {
              src: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/20d36fbaa18625e4fe507af31e4e9f83.jpg?thumb=1&w=250&h=250&f=webp&q=90',
              title: '全面屏电视E43K',
              desc: '全面屏设计，海量内容',
              price: {
                cur: '1399',
                del: '1599'
              }
            },
          ],
          [
            {
              src: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/f193daba3989eadac5e13ae102b91582.jpg?thumb=1&w=250&h=250&f=webp&q=90',
              title: '全面屏电视 55英寸E55X',
              desc: '潮流全面屏设计',
              price: {
                cur: '2299',
                del: '2599'
              }
            },
          ]
        ]
      },
      {
        title: '智能',
        img: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/a4ba966c8347c103ef9a4c87409aaa1b.jpg?thumb=1&w=1533&h=150&f=webp&q=90',
        moreList: [
          '热门',
          '安防',
          '出行'
        ],
        shoppingThumb: [
          'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/116fc43816b87192be4e67cf762e8da5.jpeg?thumb=1&w=293&h=375&f=webp&q=90',
          'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/dfbdabe36b2d630d57a015e6fb5eb3ea.jpg?thumb=1&w=293&h=375&f=webp&q=90'
        ],
        shoppingItems: [
          [
            {
              src: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/20d36fbaa18625e4fe507af31e4e9f83.jpg?thumb=1&w=250&h=250&f=webp&q=90',
              title: '全面屏电视E43K',
              desc: '全面屏设计，海量内容',
              price: {
                cur: '1399',
                del: '1599'
              }
            },
          ],
          [
            {
              src: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/f193daba3989eadac5e13ae102b91582.jpg?thumb=1&w=250&h=250&f=webp&q=90',
              title: '全面屏电视 55英寸E55X',
              desc: '潮流全面屏设计',
              price: {
                cur: '2299',
                del: '2599'
              }
            },
          ]
        ]
      },
      {
        title: '配件',
        img: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/66523a1accdc72e01c01d4761a26fbb9.jpg?thumb=1&w=1533&h=150&f=webp&q=90',
        moreList: [
          '热门',
          '充电器'
        ],
        shoppingThumb: [
          'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/9f64bbd58c3f5001bdf0688894f22cb6.jpg?thumb=1&w=293&h=375&f=webp&q=90',
          'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/ffe4182f1d9a5befdf2380ec90ae1620.jpg?thumb=1&w=293&h=375&f=webp&q=90'
        ],
        shoppingItems: [
          [
            {
              src: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/20d36fbaa18625e4fe507af31e4e9f83.jpg?thumb=1&w=250&h=250&f=webp&q=90',
              title: '全面屏电视E43K',
              desc: '全面屏设计，海量内容',
              price: {
                cur: '1399',
                del: '1599'
              }
            },
          ],
          [
            {
              src: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/f193daba3989eadac5e13ae102b91582.jpg?thumb=1&w=250&h=250&f=webp&q=90',
              title: '全面屏电视 55英寸E55X',
              desc: '潮流全面屏设计',
              price: {
                cur: '2299',
                del: '2599'
              }
            },
          ]
        ]
      },
      {
        title: '周边',
        img: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/88e35cffc82cd98cd53172460067af17.jpg?thumb=1&w=1533&h=150&f=webp&q=90',
        moreList: [
          '热门',
          '出行'
        ],
        shoppingThumb: [
          'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/ca0940f052227d235e7de5678d106c89.jpg?thumb=1&w=293&h=375&f=webp&q=90',
          'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/0497ba8520dc4aca9d55e6b841d42331.jpg?thumb=1&w=293&h=375&f=webp&q=90'
        ],
        shoppingItems: [
          [
            {
              src: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/20d36fbaa18625e4fe507af31e4e9f83.jpg?thumb=1&w=250&h=250&f=webp&q=90',
              title: '全面屏电视E43K',
              desc: '全面屏设计，海量内容',
              price: {
                cur: '1399',
                del: '1599'
              }
            },
          ],
          [
            {
              src: 'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/f193daba3989eadac5e13ae102b91582.jpg?thumb=1&w=250&h=250&f=webp&q=90',
              title: '全面屏电视 55英寸E55X',
              desc: '潮流全面屏设计',
              price: {
                cur: '2299',
                del: '2599'
              }
            },
          ]
        ]
      },
    ])

    return { shoppings }
  }
}
</script>

<style>
.content {
  background-color: #f5f5f5;
  padding-bottom: 31px;
}

.mm-content__seckill {
  position: relative;
  margin-bottom: 8px;
}

.mm-content__seckill--tbar {
  height: 58px;
}

.mm-content__seckill--tbar h2 {
  font-size: 22px;
  font-family: Helvetica Neue;
  color: #333;
  line-height: 58px;
  font-weight: 200;
}

.seckill-swiper__btn {
  position: absolute;
  right: 0;
  top: 24px;
}

.seckill-swiper__btn span {
  display: inline-block;
  width: 36px;
  height: 24px;
  padding: 3px 5px;
  margin-left: -1px;
  border: 1px solid #e0e0e0;
  font-size: 16px;
  line-height: 16px;
  -webkit-transition: color .5s;
  transition: color .5s;
  color: #b0b0b0;
  text-align: center;
  cursor: pointer;
}

.seckill-swiper__btn span:hover {
  color: #ff6700;
}

.seckill-swiper__btn span .disabled {
  color: #e0e0e0;
  cursor: default;
}

.seckill-swiper__btn span:hover .disabled {
  color: none;
}

.seckill-swiper__thumb {
  border-top-width: 1px;
  border-top-style: solid;
  border-top-color: #e53935;
  float: left;
  width: 234px;
  height: 340px;
  background-color: #f1eded;
  padding: 39px 0px 0px;
  text-align: center;
}

.seckill-swiper__thumb .seckill-swiper__thumb--round {
  display: block;
  color: #ef3a3b;
  font-size: 21px;
  line-height: 31.5px;
  padding: 15px 0px 0px;
  text-align: center;
}

.mm-content__seckill .seckill-swiper__thumb img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 34px;
  height: 53px;
  margin-bottom: 31px;
}

.seckill-swiper__thumb .seckill-swiper__thumb--desc {
  color: rgba(0,0,0,.54);
  font-size: 15px;
}

.seckill-swiper__thumb--coutdown {
  width: 168px;
  margin: 28px auto 0;
}

.seckill-swiper__thumb--coutdown span {
  display: inline-block;
  width: 46px;
  height: 46px;
  background-color: #605751;
  color: #ffffff;
  font-size: 24px;
  line-height: 46px;
  text-align: center;
}

.seckill-swiper__thumb--coutdown i {
  display: inline-block;
  width: 15px;
  height: 46px;
  line-height: 46px;
  color: #605751;
  font-size: 28px;
  font-style: normal;
}

.seckill-swiper__shopping {
  width: 992px;
  height: 340px;
  overflow: hidden;
  display: flex;
}

.mm-content__seckill img {
  margin-top: 22px;
  width: 1226px;
  height: 120px;
}
</style>