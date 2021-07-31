<template>
  <div class="mm-shopping">
    <div class="mm-shopping__hd">
      <h2>{{ shoppingTitle }}</h2>
      <div class="shopping-hd__more">
        <ul>
          <li v-for="(more, index) in moreList" :key="index" @mouseover="tab = index" :class="{ 'hd-more__active': tab == index }">
            {{ more }}
          </li>
        </ul>
      </div>
    </div>

    <div class="mm-shopping__thumb">
      <a href="">
        <img :src="shoppingThumb[0]" alt="">
      </a>
      <a href="">
        <img :src="shoppingThumb[1]" alt="">
      </a>
    </div>
    <div v-for="(shoppingItem, index) in shoppingItems" :key="index" class="mm-shopping__item" v-show="tab == index">
      <a v-for="(item, index) in shoppingItem" :key="index" href="">
        <div class="shopping-item__content">
          <img :src="item.src" alt="">
          <h3>{{ item.title }}</h3>
          <p class="content-desc">{{ item.desc }}</p>
          <p class="content-price">
            <span>{{ item.price.cur }}</span>元起
            <del>{{ item.price.del }}元</del>
          </p>
        </div>
      </a>
    </div>
    <img class="shopping-img" :src="shoppingImg" alt="">
  </div>
</template>

<script>
import { reactive, ref } from '@vue/reactivity'
export default {
  name: 'MiShopping',
  props: {
    title: String,
    list: Object,
    items: Object,
    thumb: Object,
    img: String
  },
  setup(props) {
    // console.log("props", props);
    let tab = ref(0);
    const shoppingImg = ref(props.img)
    const shoppingTitle = ref(props.title)
    const moreList = reactive(props.list);
    // console.log("moreList", moreList);
    const shoppingItems = reactive(props.items);
    const shoppingThumb = reactive(props.thumb)
    // console.log(shoppingThumb);

    return { shoppingTitle, tab, shoppingItems, moreList, shoppingImg, shoppingThumb }
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
}

.shopping-hd__more ul {
  padding: 16px 0 0;
  font-size: 16px;
}

.shopping-hd__more li {
  float: left;
  margin-left: 30px;
  cursor: pointer;
}

.shopping-hd__more li:hover {
  color: #ff6700;
  border-bottom: 2px solid #ff6700;
}

.hd-more__active {
  color: #ff6700;
  border-bottom: 2px solid #ff6700;
}

.mm-shopping__thumb {
  float: left;
  width: 234px;
}
.mm-shopping__thumb img {
  width: 234px;
  height: 300px;
  transition: all .2s linear;
  margin-bottom: 7px;
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