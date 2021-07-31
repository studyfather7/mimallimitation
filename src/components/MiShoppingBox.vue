<template>
  <a
    :style="boxPerStyle"
    class="box">
    <div class="box-content">
      <img class="box-thumb" :src="img" alt="">
      <h3 class="box-title">{{ title }}</h3>
      <p class="box-desc">{{ desc }}</p>
      <p class="box-price">
        <span class="box-price__cur">{{ price.cur }}</span>元<span v-if="boxIsPrice">起</span>
        <del class="box-price__del">{{ price.del }}</del>
      </p>
    </div>
  </a>
</template>

<script>
import { reactive ,toRefs, ref } from '@vue/reactivity'
export default {
  name: "MiShoppingBox",
  props: {
    content: Object,
    isPrice: Boolean,
    perStyle: Object
  },
  setup(props) {
    const boxContent = reactive(props.content)
    const boxPerClass = reactive(props.perClass)
    const boxIsPrice = ref(props.isPrice)
    const boxPerStyle = reactive(props.perStyle)
    return {
       ...toRefs(boxContent),
       boxPerClass,
       boxIsPrice,
       boxPerStyle
    }
  }
}
</script>

<style lang="scss" scoped>
.box {
  display: inline-block;
  text-decoration: none;
  width: 234px;
  height: 340px;
  background-color: #fff;
  text-align: center;
  margin-left: calc(56px / 4);
  padding: 20px 0;
  &-thumb {
    width: 160px;
    height: 160px;
  }
  &-title {
    text-overflow: ellipsis;
    white-space: nowrap;
    overflow: hidden;    font-size: 14px;
    font-weight: 400;
    color: #333;
    margin: 0 10px 2px;
  }
  &-desc {
    margin: 0 10px 10px;
    height: 18px;
    font-size: 12px;
    color: #b0b0b0;
    text-align: center;
    text-overflow: ellipsis;
    white-space: nowrap;
    overflow: hidden;
  }
  &-price {
    margin: 0 10px 14px;
    color: #ff6700;
    font-size: 14px;
    &__del {
      margin-left: .5em;
      color: #b0b0b0;
    }
  }
}

.seckill-box {
  flex-grow:0;
  flex-shrink:0;
  border-top: 1px solid;
  transition: all .7s ease-in-out;
}
</style>