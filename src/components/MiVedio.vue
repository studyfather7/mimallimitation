<template>
  <div class="mm-vedio">
    <div class="mm-shopping__hd">
      <h2>视频</h2>
      <div class="shopping-hd__more">
        <a href="">查看全部</a>
        <i class="iconfont iconfont-arrow-right-big"></i>
      </div>
    </div>

    <div class="mi-vedio-content">
      <div class="box">
        <a href="">
          <div class="box-thumb">
            <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/e74c4ff741bcdfc5b28a48a43e4edc6d.jpg?thumb=1&w=370&h=225&f=webp&q=90" alt="">
            <span class="play"><i class="iconfont-play"></i></span>
          </div>
          <h3>2021年春季新品发布会第一场</h3>
        </a>
      </div>
      <div class="box">
        <a href="">
          <div class="box-thumb">
            <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/e74c4ff741bcdfc5b28a48a43e4edc6d.jpg?thumb=1&w=370&h=225&f=webp&q=90" alt="">
            <span class="play"><i class="iconfont-play"></i></span>
          </div>
          <h3>2021年春季新品发布会第一场</h3>
        </a>
      </div>
      <div class="box">
        <a href="">
          <div class="box-thumb">
            <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/e74c4ff741bcdfc5b28a48a43e4edc6d.jpg?thumb=1&w=370&h=225&f=webp&q=90" alt="">
            <span class="play"><i class="iconfont-play"></i></span>
          </div>
          <h3>2021年春季新品发布会第一场</h3>
        </a>
      </div>
      <div class="box">
        <a href="">
          <div class="box-thumb">
            <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/e74c4ff741bcdfc5b28a48a43e4edc6d.jpg?thumb=1&w=370&h=225&f=webp&q=90" alt="">
            <span class="play"><i class="iconfont-play"></i></span>
          </div>
          <h3>2021年春季新品发布会第一场</h3>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MiVedio',

}
</script>

<style lang='scss'>
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

.mi-vedio-content {
  display: grid;
  grid-template-columns: repeat(1fr, 4);
  grid-column-gap: 14px;
  grid-auto-flow: column;
  & .box {
    width: 296px;
    height: 253px;
    background-color: #fff;
    transition: all .2s linear;
    &:hover {
      z-index: 2;
      -webkit-box-shadow: 0 15px 30px rgb(0 0 0 / 10%);
      box-shadow: 0 15px 30px rgb(0 0 0 / 10%);
      -webkit-transform: translate3d(0,-2px,0);
      transform: translate3d(0,-2px,0);
      & .play {
        background-color: #ff6700;
        border: 2px solid #ff6700;
      }
    }
    &-thumb {
      position: relative;
      margin: 0 0 28px;
      height: 180px;
      width: inherit;
    }
    & a {
      position: relative;
      width: inherit;
      height: inherit;
      & img {
        height: 180px;
        width: inherit;
      }
      & h3 {
        margin: 0 14px 6px;
        font-size: 14px;
        font-weight: 400;
        text-align: center;
        color: #333;
        white-space: nowrap;
        text-overflow: ellipsis;
        overflow: hidden;
      }
    }
  }
}


.play {
  box-sizing: content-box;
  position: absolute;
  left: 20px;
  bottom: 10px;
  width: 32px;
  height: 20px;
  border: 2px solid #fff;
  border-radius: 12px;
  background-color: #424242;
  background-color: rgba(0,0,0,.6);
  color: #fff;
  -webkit-transition: all .2s;
  transition: all .2s;
  overflow: hidden;
  & i {
    font-size: 30px;
    line-height: 20px;
  }
}

a:hover {
  color: #ff6700;
}
</style>