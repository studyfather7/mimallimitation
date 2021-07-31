<template>
  <div class="mm-content__seckill">
    <div class="mm-content__seckill--tbar">
      <h2>小米秒杀</h2>
    </div>
    <div class="mm-content__seckill--swiper">
      <div class="seckill-swiper__thumb">
        <span class="seckill-swiper__thumb--round">14:00场</span>
        <img src="data:img/jpg;base64,iVBORw0KGgoAAAANSUhEUgAAACIAAAA1CAYAAAAklDnhAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJ%0AbWFnZVJlYWR5ccllPAAAAyNpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdp%0Abj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6%0AeD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuNS1jMDE0IDc5LjE1%0AMTQ4MSwgMjAxMy8wMy8xMy0xMjowOToxNSAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJo%0AdHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlw%0AdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAv%0AIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RS%0AZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpD%0AcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENDIChNYWNpbnRvc2gpIiB4bXBNTTpJbnN0YW5j%0AZUlEPSJ4bXAuaWlkOjY4Q0ZFMkY5MTJFNzExRThCMkM4OEM1RTNBNjczQUVBIiB4bXBNTTpEb2N1%0AbWVudElEPSJ4bXAuZGlkOjY4Q0ZFMkZBMTJFNzExRThCMkM4OEM1RTNBNjczQUVBIj4gPHhtcE1N%0AOkRlcml2ZWRGcm9tIHN0UmVmOmluc3RhbmNlSUQ9InhtcC5paWQ6NjhDRkUyRjcxMkU3MTFFOEIy%0AQzg4QzVFM0E2NzNBRUEiIHN0UmVmOmRvY3VtZW50SUQ9InhtcC5kaWQ6NjhDRkUyRjgxMkU3MTFF%0AOEIyQzg4QzVFM0E2NzNBRUEiLz4gPC9yZGY6RGVzY3JpcHRpb24+IDwvcmRmOlJERj4gPC94Onht%0AcG1ldGE+IDw/eHBhY2tldCBlbmQ9InIiPz5oEyacAAACoklEQVR42sSYv0tbURTHX0LqD6T4g4pE%0AcHDoUOloBxVd/QFFEcQqWtrSKlKFmmAslopohzgIbv4FwUEE0clFujiIi+BSIbRQ0ooKRReRULHf%0AS48Qgu++c3/FAx+iyU3eJzf3nnPuC/1qavQ04zVY8szjCHRGNN9cBD6DSkOJKzAGzsOaH/AW1FuY%0AjRg4EH/oiJSCTxYk1sDK7T86Iu9BraHED/Au9wlVkYdg2lAiC/rBhYnIB/DIUOQj2M9/UkWkCsQN%0AJbbA8l0vqIhMgXIDiZ/gFbgxEakBEwYSf8Eg+OM3gCsyA8oMRETy25UN4IjUgVEDiW2wGDSIIzIL%0AijUljsFLv3WhIvKYFphOXNO6OOUMDhKZA7qFcQF85Q6WXeQpeKEpcULlvY8xthp8iwR8I93qLLb7%0AKnOsSPWNfhd6Bro99yHqTi9IhyWzEXIsIXbSG7Djt1jbQHsBZkMkyZRs13wpgIRoiJKy7dsBWh1L%0AbN5Vt3JFQrQ2XMYeGKBk5yvSI7aRQ4k0eA4uZZlVPM47lDgTZxd6lKb4AcqkLuKSZiIdVGsiVFNc%0AxDV9yT1Orekjoe+MDw4pHqwmaJewit66Ql0QaX+DOTaZe4DitAFZxQaaEynKnJ6KCDeaQAtj3A7V%0AkBtXIpwT3iFV06zqquaKPKEtKIsM6Mo/StoWiQeMvSCJjO4+54hEwTCjuTk0STgckUm6QxTY3LgU%0AKc+/jyFrblyKCIkKbnPjSkT8HDGV5saVyBAtVHZz40Ik7HNTRtrcuBARF2tQbW5ciCR0mhvbIs2E%0AcnNjWySh29zYFGnIK25KzY1Nkdziptzc2BKJUu7Qbm5sicQom2o3NzZEKqiu/DZpbmyIjIAHNBMZ%0A7x4iTALjhcgVQSIl3v87w5vePcY/AQYAFYR6skFSqBUAAAAASUVORK5CYII=" alt="">
        <span class="seckill-swiper__thumb--desc">距离结束还有</span>
        <div class="seckill-swiper__thumb--coutdown">
          <span>03</span>
          <i>:</i>
          <span>33</span>
          <i>:</i>
          <span>32</span>
        </div>
      </div>
      <div class="seckill-swiper__shopping">
        <template v-for="(shopping, index) in shoppings" :key="index">
          <mi-shopping-box
          class="seckill-box"
          :content="shopping"
          :style="perStyle(index)"
          ></mi-shopping-box>
        </template>
      </div>
      <div class="seckill-swiper__btn">
        <span 
          @click="prev">
          <i class="iconfont-arrow-left-big" :class="{ disabled: this.idx == 4}"></i>
        </span>
        <span 
          @click="next">
          <i class="iconfont-arrow-right-big" :class="{ disabled: this.idx == shoppings.length }"></i>
        </span>
      </div>
    </div>
    <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/431e5fd6bfd1b67d096928248be18303.jpg?thumb=1&w=1533&h=150&f=webp&q=90" alt="">
  </div>
</template>

<script>
import MiShoppingBox from './MiShoppingBox.vue'
export default {
  name: 'MiSeckill',
  components: { MiShoppingBox },
  data() {
    return {
      colors: [
        "#ffac13",
        "#83c44e",
        "#2196f3",
        "#e53935",
        "#00c0a5"
      ],
      idx: 4,
      shoppings: [
        {
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/730055892c1afa7b6d8128c0938b5277.png?thumb=1&w=200&h=200&f=webp&q=90",
          title: "日常元素抽纸 青春版 24包/箱",
          desc: "精选原生竹浆，健康环保",
          price: {
            cur: "25.9",
            del: "32.9元"
          }
        },
        {
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/730055892c1afa7b6d8128c0938b5277.png?thumb=1&w=200&h=200&f=webp&q=90",
          title: "日常元素抽纸 青春版 24包/箱",
          desc: "精选原生竹浆，健康环保",
          price: {
            cur: "25.9",
            del: "32.9元"
          }
        },
        {
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/730055892c1afa7b6d8128c0938b5277.png?thumb=1&w=200&h=200&f=webp&q=90",
          title: "日常元素抽纸 青春版 24包/箱",
          desc: "精选原生竹浆，健康环保",
          price: {
            cur: "25.9",
            del: "32.9元"
          }
        },
        {
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/730055892c1afa7b6d8128c0938b5277.png?thumb=1&w=200&h=200&f=webp&q=90",
          title: "日常元素抽纸 青春版 24包/箱",
          desc: "精选原生竹浆，健康环保",
          price: {
            cur: "25.9",
            del: "32.9元"
          }
        },
        {
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/730055892c1afa7b6d8128c0938b5277.png?thumb=1&w=200&h=200&f=webp&q=90",
          title: "日常元素抽纸 青春版 24包/箱",
          desc: "精选原生竹浆，健康环保",
          price: {
            cur: "25.9",
            del: "32.9元"
          }
        },
        {
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/730055892c1afa7b6d8128c0938b5277.png?thumb=1&w=200&h=200&f=webp&q=90",
          title: "日常元素抽纸 青春版 24包/箱",
          desc: "精选原生竹浆，健康环保",
          price: {
            cur: "25.9",
            del: "32.9元"
          }
        },
        {
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/730055892c1afa7b6d8128c0938b5277.png?thumb=1&w=200&h=200&f=webp&q=90",
          title: "日常元素抽纸 青春版 24包/箱",
          desc: "精选原生竹浆，健康环保",
          price: {
            cur: "25.9",
            del: "32.9元"
          }
        },
        {
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/730055892c1afa7b6d8128c0938b5277.png?thumb=1&w=200&h=200&f=webp&q=90",
          title: "日常元素抽纸 青春版 24包/箱",
          desc: "精选原生竹浆，健康环保",
          price: {
            cur: "25.9",
            del: "32.9元"
          }
        },
        {
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/730055892c1afa7b6d8128c0938b5277.png?thumb=1&w=200&h=200&f=webp&q=90",
          title: "日常元素抽纸 青春版 24包/箱",
          desc: "精选原生竹浆，健康环保",
          price: {
            cur: "25.9",
            del: "32.9元"
          }
        },
        {
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/730055892c1afa7b6d8128c0938b5277.png?thumb=1&w=200&h=200&f=webp&q=90",
          title: "日常元素抽纸 青春版 24包/箱",
          desc: "精选原生竹浆，健康环保",
          price: {
            cur: "25.9",
            del: "32.9元"
          }
        },
        {
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/730055892c1afa7b6d8128c0938b5277.png?thumb=1&w=200&h=200&f=webp&q=90",
          title: "日常元素抽纸 青春版 24包/箱",
          desc: "精选原生竹浆，健康环保",
          price: {
            cur: "25.9",
            del: "32.9元"
          }
        },
        {
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/730055892c1afa7b6d8128c0938b5277.png?thumb=1&w=200&h=200&f=webp&q=90",
          title: "日常元素抽纸 青春版 24包/箱",
          desc: "精选原生竹浆，健康环保",
          price: {
            cur: "25.9",
            del: "32.9元"
          }
        },
        {
          img: "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/730055892c1afa7b6d8128c0938b5277.png?thumb=1&w=200&h=200&f=webp&q=90",
          title: "日常元素抽纸 青春版 24包/箱",
          desc: "精选原生竹浆，健康环保",
          price: {
            cur: "25.9",
            del: "32.9元"
          }
        },
      ],
    }
  },
  methods: {
    perStyle(index) {
      return {
        borderTopColor: `${this.colors[index % 4]}`, 
        transform: `translateX(${-(this.idx - 4) * 248}px)`   
      }
    },
    prev() {
      this.idx - 4 > 4 ? this.idx -= 4 : this.idx = 4 
      if (this.timer) {
        clearInterval(this.timer)
      }
    },
    next() {
      if (this.idx >= this.shoppings.length) {
        return;
      }
      this.shoppings.length - this.idx > 4 ? this.idx += 4 : this.idx = this.shoppings.length
      if (this.timer) {
        clearInterval(this.timer)
      }
    }
  },
  mounted() {
    this.timer = setInterval(() => {
      // console.log('length', this.shoppings.length);
      // console.log('idx', this.idx);
      if (this.idx >= this.shoppings.length) {
        this.idx = 4
        return
      }
      this.shoppings.length - this.idx > 4 ? this.idx += 4 : this.idx = this.shoppings.length
    }, 5000)
  },
}
</script>

<style>

</style>