<template>
  <div data-v-212c8a9d="" class="home-tool-bar home-tool-bar-large">
    <a
      data-v-212c8a9d=""
      data-spm="toolbar.3343648.1"
      data-log_code="bid=3343648"
      class="item item-image"
      data-params='""'
      data-settrack="true"
      onclick="_msq.push(['trackEvent','bid=3343648','','81190ccc4d52f577-00','&quot;&quot;']);"
      ><div data-v-212c8a9d="" class="icon">
        <img
          data-v-212c8a9d=""
          src="https://i8.mifile.cn/b2c-mimall-media/98a23aae70f25798192693f21c4d4039.png"
          class="static"
        />
        <img
          data-v-212c8a9d=""
          src="https://i8.mifile.cn/b2c-mimall-media/74c4fcb4475af8308e9a670db9c01fdf.png"
          class="hover"
        />
      </div>
      <span data-v-212c8a9d="" class="text"> 手机APP<!----></span>
      <div data-v-212c8a9d="" class="pop-content">
        <img
          data-v-212c8a9d=""
          src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/78c30d4f259ed43ab20e810a522a6249.png"
        /><span data-v-212c8a9d="" class="desc"> 扫码领取新人百元礼包 </span>
      </div>
      <!----></a
    >
    <a
      data-v-212c8a9d=""
      data-spm="toolbar.3213221.1"
      data-log_code="bid=3213221"
      class="item"
      data-params='""'
      data-settrack="true"
      onclick="_msq.push(['trackEvent','bid=3213221','','81190ccc4d52f577-00','&quot;&quot;']);"
      ><div data-v-212c8a9d="" class="icon">
        <img
          data-v-212c8a9d=""
          src="https://i8.mifile.cn/b2c-mimall-media/55cad219421bee03a801775e7309b920.png"
          class="static"
        /><img
          data-v-212c8a9d=""
          src="https://i8.mifile.cn/b2c-mimall-media/41f858550f42eb1770b97faf219ae215.png"
          class="hover"
        />
      </div>
      <span data-v-212c8a9d="" class="text"> 个人中心<!----></span
      ><!----><!----></a
    >
    <a
      data-v-212c8a9d=""
      data-spm="toolbar.3213225.1"
      data-log_code="bid=3213225"
      class="item"
      data-params='""'
      data-settrack="true"
      onclick="_msq.push(['trackEvent','bid=3213225','','81190ccc4d52f577-00','&quot;&quot;']);"
      ><div data-v-212c8a9d="" class="icon">
        <img
          data-v-212c8a9d=""
          src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/12eb0965ab33dc8e05870911b90f3f13.png"
          class="static"
        /><img
          data-v-212c8a9d=""
          src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/95fbf0081a06eec7be4d35e277faeca0.png"
          class="hover"
        />
      </div>
      <span data-v-212c8a9d="" class="text"> 售后服务<!----></span
      ><!----><!----></a
    >
    <a
      data-v-212c8a9d=""
      data-spm="toolbar.3213222.1"
      data-log_code="bid=3213222"
      class="item"
      data-params='""'
      data-settrack="true"
      onclick="_msq.push(['trackEvent','bid=3213222','','81190ccc4d52f577-00','&quot;&quot;']);"
      ><div data-v-212c8a9d="" class="icon">
        <img
          data-v-212c8a9d=""
          src="https://i8.mifile.cn/b2c-mimall-media/4f036ae4d45002b2a6fb6756cedebf02.png"
          class="static"
        /><img
          data-v-212c8a9d=""
          src="https://i8.mifile.cn/b2c-mimall-media/5e9f2b1b0da09ac3b3961378284ef2d4.png"
          class="hover"
        />
      </div>
      <span data-v-212c8a9d="" class="text"> 人工客服<!----></span
      ><!----><!----></a
    ><a
      data-v-212c8a9d=""
      data-spm="toolbar.3213223.1"
      data-log_code="bid=3213223"
      class="item"
      data-params='""'
      data-settrack="true"
      onclick="_msq.push(['trackEvent','bid=3213223','','81190ccc4d52f577-00','&quot;&quot;']);"
      ><div data-v-212c8a9d="" class="icon">
        <img
          data-v-212c8a9d=""
          src="https://i8.mifile.cn/b2c-mimall-media/d7db56d1d850113f016c95e289e36efa.png"
          class="static"
        /><img
          data-v-212c8a9d=""
          src="https://i8.mifile.cn/b2c-mimall-media/692a6c3b0a93a24f74a29c0f9d68ec71.png"
          class="hover"
        />
      </div>
      <span data-v-212c8a9d="" class="text"> 购物车<!----></span
      ><!----><!----></a
    ><!---->
    <a
      @click="backtop()"
      v-show="scrollTop > 100"
      data-v-212c8a9d=""
      data-spm="toolbar.to_top_float.1"
      href="javascript:void(0);"
      data-log_code="bid=3212729"
      class="item backtop active"
      data-params='""'
      ><div data-v-212c8a9d="" class="icon">
        <img
          data-v-212c8a9d=""
          src="//i1.mifile.cn/f/i/2018/home/totop.png"
          class="static"
        /><img
          data-v-212c8a9d=""
          src="//i1.mifile.cn/f/i/2018/home/totop_hover.png"
          class="hover"
        />
      </div>
      <span data-v-212c8a9d="" class="text">回顶部</span></a
    >
  </div>
</template>

<script>
import { ref } from '@vue/reactivity';
import { onMounted } from '@vue/runtime-core';
export default {
  name: "MiSidebar",
  setup() {
    let scrollTop = ref(0);

    function backtop(){
      var timer = setInterval(function(){
        let osTop = document.documentElement.scrollTop || document.body.scrollTop;
        let ispeed = Math.floor(-osTop / 5); 
        document.documentElement.scrollTop = document.body.scrollTop = osTop + ispeed;
        this.isTop = true;
        if(osTop === 0){
          clearInterval(timer);
        }
      },30)
    }

    onMounted(() => {
      window.addEventListener('scroll', () => {
        scrollTop.value = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop;
      })
    })

    return { scrollTop, backtop }
  }
};
</script>

<style lang='scss' scoped>
.home-tool-bar[data-v-212c8a9d] {
  position: fixed;
  bottom: 70px;
  right: 0;
  z-index: 99;
}

.home-tool-bar .item[data-v-212c8a9d] {
  position: relative;
  display: block;
  width: 82px;
  height: 90px;
  margin-top: -1px;
  background-color: #fff;
  border: 1px solid #f5f5f5;
  text-align: center;
}

.home-tool-bar .item .icon[data-v-212c8a9d] {
  position: relative;
  width: 30px;
  height: 30px;
  margin: 0 auto 8px;
  padding-top: 18px;
  box-sizing: content-box;
}

.home-tool-bar .item .text[data-v-212c8a9d] {
  color: #757575;
  -webkit-transition: color 0.3s;
  transition: color 0.3s;
}

.home-tool-bar .item .pop-content[data-v-212c8a9d] {
    position: absolute;
    left: 0;
    top: 0;
    padding: 14px;
    background: #fff;
    border: 1px solid #f5f5f5;
    -webkit-transition: opacity .3s;
    transition: opacity .3s;
    -webkit-transform: translateZ(0);
    transform: translateZ(0);
    opacity: 0;
    visibility: hidden;
}

.home-tool-bar .item .pop-content img[data-v-212c8a9d] {
  display: block;
  width: 100px;
  height: 100px;
  margin: 6px auto;
}

.home-tool-bar .item .pop-content .desc[data-v-212c8a9d] {
    display: block;
    width: 82px;
    margin: 14px auto 0;
    color: #757575;
    text-align: center;
}

.home-tool-bar .item:hover .pop-content[data-v-212c8a9d] {
    -webkit-transform: translate3d(-110%,0,0);
    transform: translate3d(-110%,0,0);
    opacity: 1;
    visibility: visible;
}

.home-tool-bar .item .icon img {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 30px;
  height: 30px;
  -webkit-transition: opacity 0.3s;
  transition: opacity 0.3s;
  opacity: 0;
  &.static {
    opacity: 1;
  }
}

.home-tool-bar .item:hover {
  .hover {
    opacity: 1;
  }
  .text {
    color: #ff6700;
  }
  .pop-content {
    opacity: 1;
    visibility: visible;
  }
}

.home-tool-bar .backtop[data-v-212c8a9d] {
  margin-top: 14px;
  border-top: 1px solid #f5f5f5;
}
</style>