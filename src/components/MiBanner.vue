<template>
<div class="show">
  <div class="wrapper">
    <div class="mm-banner">
        <div class="mm-banner__list">
          <ul>
            <li
              @mouseover="items[idx].active = true"
              @mouseout="items[idx].active = false"
              :class="{ active: items[idx].active }"
              class="banner-list__item"
              v-for="(item, idx) in items"
              :key="idx"
            >
              <a href="">
                {{ item.name }}
              </a>
              <em class="iconfont-arrow-right-big"></em>
              <div class="list-item__showcase">
                <a v-for="acase in item.cases" :key="acase">
                  <img :src="acase.src" class="item-showcase__thumb" />
                  <span class="item-showcase__text">{{ acase.text }}</span>
                </a>
              </div>
            </li>
          </ul>
        </div>
        <div class="mm-banner__carousel">
          <div class="banner-carousel__content">
            <a href="">
              <img :src="imgs[num]" alt="" />
            </a>
          </div>
          <div class="banner-carousel__pagination">
            <span
              :class="{ active: this.num == i - 1 }"
              v-for="i in imgs.length"
              :key="i"
              @click="select(i)"
            ></span>
          </div>
          <div
            class="banner-carousel__prev carousel-btn"
            @click="num == 0 ? (num = imgs.length - 1) : num--"
          ></div>
          <div
            class="banner-carousel__next carousel-btn"
            @click="num == imgs.length - 1 ? (num = 0) : num++"
          ></div>
        </div>
    </div>
    <div class="mm-show__sub">
      <div class="mm-show__sub--6in1">
        <a v-for="span in spans" :key="span" href="">
          <img :src="span.img" alt="">
          {{ span.text }}
        </a>
      </div>
      <div class="mm-show__sub--3block">
        <ul>
          <li v-for="(subImg, index) in subImgs" :key="index">
            <a href="">
              <img :src="subImg" alt="">
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</div>


</template>

<script>
export default {
  name: "MmBanner",
  data() {
    return {
      imgs: [
        "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/d7abb68ac50f82412d325f305cc62fb0.jpeg?w=2452&h=920",
        "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/02b6f2a85191a4806e6fefb38a12890a.jpg?thumb=1&w=1533&h=575&f=webp&q=90",
        "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/1c3e97686468231f3f78048d7f2b7fdc.jpg?thumb=1&w=1533&h=575&f=webp&q=90",
        "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/7f2e0acc18c3d9b6a9c1ab9e8281fbd6.jpg?thumb=1&w=1533&h=575&f=webp&q=90",
      ],
      subImgs: [
        "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/5d4298059889417157e8492750328492.jpg?w=632&h=340",
        "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/b30177d629bfbe2fb42251c1b8538f7b.jpg?w=632&h=340",
        "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/9f18ac756fa2cedb16ea429b9c0001af.png?w=632&h=340"
      ],
      spans: [
        {
          text: "小米秒杀",
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/82abdba456e8caaea5848a0cddce03db.png?w=48&h=48",
          },
        {
          text: "企业团购",
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/806f2dfb2d27978e33fe3815d3851fa3.png?w=48&h=48",
          },
        {
          text: "F码通道",
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/eded6fa3b897a058163e2485532c4f10.png?w=48&h=48",
          },
        {
          text: "米粉卡",
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/43a3195efa6a3cc7662efed8e7abe8bf.png?w=48&h=48",
          },
        {
          text: "以旧换新",
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/f4846bca6010a0deb9f85464409862af.png?w=48&h=48",
          },
        {
          text: "话费充值",
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/9a76d7636b08e0988efb4fc384ae497b.png?w=48&h=48"
          },
      ],
      items: [
        {
          name: "手机 电话卡",
          cases: [
            {
              src: "//cdn.cnbj1.fds.api.mi-img.com/mi-mall/ab345272bf9894bb8269d4901344b068.png?thumb=1&amp;w=40&amp;h=40&amp;f=webp&amp;q=90",
              text: "小米MIX FOLD",
            },
            {
              src: "//cdn.cnbj1.fds.api.mi-img.com/mi-mall/a1241b5a94ba1739e85f72d46592af0e.png?thumb=1&amp;w=40&amp;h=40&amp;f=webp&amp;q=90",
              text: "小米11 Ultra",
            },
          ],
        },
        {
          name: "电视 盒子",
        },
        {
          name: "笔记本 显示器",
        },
        {
          name: "家电 插线板",
        },
        {
          name: "出行 穿戴",
        },
        {
          name: "智能 路由器",
        },
        {
          name: "电源 配件",
        },
        {
          name: "健康 儿童",
        },
        {
          name: "耳机 音箱",
        },
        {
          name: "生活 箱包",
        },
      ],
      num: 0,
    };
  },
  methods: {
    select(i) {
      // console.log(i);
      this.num = i - 1;
    },
  },
  mounted() {
    setInterval(() => {
      this.num == this.imgs.length - 1 ? (this.num = 0) : this.num++;
    }, 5000);
  },
};
</script>

<style>
@import url(../assets/css/home.c43682e3.css);
.mm-banner {
  position: relative;
  height: 460px;
}

.mm-banner__list {
  z-index: 11;
  position: absolute;
  height: 460px;
  background-color: rgba(105, 101, 101, 0.5);
  padding: 20px 0;
}

.mm-banner__list ul {
  margin: 0;
  padding: 0;
}

.mm-banner__list .banner-list__item {
  font-size: 16px;
  line-height: 42px;
  width: 243px;
  height: 42px;
  padding-left: 30px;
}

.mm-banner__list .banner-list__item:hover {
  background-color: #ff6700;
}

.mm-banner__list .banner-list__item a {
  color: #fff;
}

.mm-banner__list .banner-list__item em {
  position: absolute;
  color: #e0e0e0;
  right: 20px;
}

.mm-banner__list .list-item__showcase {
  display: none;
}

.mm-banner__list .banner-list__item.active .list-item__showcase {
  z-index: 30;
  position: absolute;
  top: 0;
  left: 243px;
  background-color: #fff;
  height: 460px;
  box-shadow: 0 8px 16px rgb(0 0 0 / 18%);

  display: grid;
  grid-auto-flow: column;
  grid-template-columns: repeat(auto-fill, 1fr);
  grid-template-rows: repeat(6, 1fr);
  justify-items: center;
  align-items: center;
}

.mm-banner__list .list-item__showcase a {
  padding: 18px 20px;
  line-height: 40px;
  height: 76px;
  width: 245px;
  color: #333;
}

.mm-banner__list .list-item__showcase a:hover {
  color: #ff6700;
}

.list-item__showcase .item-showcase__thumb {
  width: 40px;
  height: 40px;
  vertical-align: middle;
}

.list-item__showcase .item-showcase__text {
  font-size: 14px;
  margin-left: 12px;
}

.mm-banner__carousel {
  position: absolute;
  width: 1226px;
  height: 460px;
  z-index: 10;
}

.mm-banner__carousel .banner-carousel__content img {
  width: 1226px;
  height: 460px;
}

.banner-carousel__prev {
  background: url(../assets/img/icon-slides.png) no-repeat -84px 50%;
  left: 243px;
  right: auto;
}

.banner-carousel__prev:hover {
  background-position: 0 50%;
}

.banner-carousel__next {
  background: url(../assets/img/icon-slides.png) no-repeat -125px 50%;
  right: 0;
  left: auto;
}

.banner-carousel__next:hover {
  background-position: -42px 50%;
}

.carousel-btn {
  z-index: 12;
  top: 50%;
  width: 41px;
  height: 69px;
  position: absolute;
}

.banner-carousel__pagination {
  position: absolute;
  right: 30px;
  bottom: 20px;
}

.banner-carousel__pagination span {
  display: block;
  cursor: pointer;
  float: left;
  z-index: 12;
  width: 10px;
  height: 10px;
  border: 2px solid;
  border-radius: 50%;
  margin: 0 4px;
  border-color: hsla(0, 0%, 100%, 0.3);
  background: rgba(0, 0, 0, 0.4);
  opacity: 1;
}

.banner-carousel__pagination span:hover {
  background: hsla(0, 0%, 100%, 0.4);
  border-color: rgba(0, 0, 0, 0.4);
}

.banner-carousel__pagination .active {
  background: hsla(0, 0%, 100%, 0.4);
  border-color: rgba(0, 0, 0, 0.4);
}

.mm-show__sub {
  margin-top: 14px;
  margin-bottom: 26px;
}

.mm-show__sub--6in1 {
  float: left;
  height: 171px;
  width: 234px;
  background-color: #5f5750;

  display: grid;
  grid-template-rows: repeat(2, 1fr);
  grid-template-columns: repeat(3, 1fr);
  align-items: center;
  justify-items: center;
}

.mm-show__sub--6in1 a {
  text-align: center;
  color: #fff;
  opacity: .7;
  background-color: rgba(0,0,0,0);
  font-size: 12px;
}

.mm-show__sub--6in1 a:hover {
  opacity: 1;
}

.mm-show__sub--6in1 img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 10px;
  width: 24px;
  height: 24px;
}

.mm-show__sub--3block {
  height: 170px;
}

.mm-show__sub--3block img {
  width: 316px;
  height: 170px;
}

.mm-show__sub--3block li {
  float: left;
  margin-left: calc(44px / 3);
}
</style>