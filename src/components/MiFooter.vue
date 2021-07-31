<template>
  <div>
    <div class="mi-footer">
      <div class="wrapper">
        <div class="mi-footer-service">
          <a href="" style="border-left: none">
            <em class="iconfont-tool"></em>
            预约维修服务
          </a>
          <a href="">
            <em class="iconfont-circle-7"></em>
            7天无理由退货
          </a>
          <a href="">
            <em class="iconfont-circle-15"></em>
            15天免费换货
          </a>
          <a href="">
            <em class="iconfont-gift"></em>
            满69包邮
          </a>
          <a href="">
            <em class="iconfont-location"></em>
            520余家售后网点
          </a>
        </div>
        <div class="footer-links clearfix" data-metatip="true">
          <dl class="col-links col-links-first">
            <dt>帮助中心</dt>
            <dd>
              <a
                rel="nofollow"
                href="//www.mi.com/service/account/Account%20registration/"
                target="_blank"
                >账户管理</a
              >
            </dd>
            <dd>
              <a
                rel="nofollow"
                href="//www.mi.com/service/buy/SalesTime/"
                target="_blank"
                >购物指南</a
              >
            </dd>
            <dd>
              <a
                rel="nofollow"
                href="//www.mi.com/service/order/sendprogress/"
                target="_blank"
                >订单操作</a
              >
            </dd>
          </dl>
          <dl class="col-links">
            <dt>服务支持</dt>
            <dd>
              <a
                rel="nofollow"
                href="//www.mi.com/service/exchange"
                target="_blank"
                >售后政策</a
              >
            </dd>
            <dd>
              <a rel="nofollow" href="//www.mi.com/service/" target="_blank"
                >自助服务</a
              >
            </dd>
            <dd>
              <a
                rel="nofollow"
                href="//www.mi.com/service/download/"
                target="_blank"
                >相关下载</a
              >
            </dd>
          </dl>
          <dl class="col-links">
            <dt>线下门店</dt>
            <dd>
              <a
                rel="nofollow"
                href="//www.mi.com/service/mihome/list"
                target="_blank"
                >小米之家</a
              >
            </dd>
            <dd>
              <a
                rel="nofollow"
                href="//www.mi.com/service/sitelist"
                target="_blank"
                >服务网点</a
              >
            </dd>
            <dd>
              <a
                rel="nofollow"
                href="//www.mi.com/service/family-location"
                target="_blank"
                >授权体验店</a
              >
            </dd>
          </dl>
          <dl class="col-links">
            <dt>关于小米</dt>
            <dd>
              <a rel="nofollow" href="//www.mi.com/about/" target="_blank"
                >了解小米</a
              >
            </dd>
            <dd>
              <a rel="nofollow" href="//hr.xiaomi.com/" target="_blank"
                >加入小米</a
              >
            </dd>
            <dd>
              <a
                rel="nofollow"
                href="//company.mi.com/zh-cn/ir/indexContent/index.html"
                target="_blank"
                >投资者关系</a
              >
            </dd>
            <dd>
              <a rel="nofollow" href="//www.mi.com/csr/" target="_blank"
                >企业社会责任</a
              >
            </dd>
            <dd>
              <a rel="nofollow" href="//www.mi.com/integrity" target="_blank"
                >廉洁举报</a
              >
            </dd>
          </dl>
          <dl class="col-links">
            <dt>关注我们</dt>
            <dd>
              <a
                rel="nofollow"
                href="//weibo.com/xiaomishangcheng"
                target="_blank"
                >新浪微博</a
              >
            </dd>
            <dd>
              <a rel="nofollow" href="javascript:void(0);" id="J_siteWeixinCode"
                >官方微信</a
              >
            </dd>
            <dd>
              <a rel="nofollow" href="//www.mi.com/about/contact/" target="_blank"
                >联系我们</a
              >
            </dd>
            <dd>
              <a
                rel="nofollow"
                href="//www.mi.com/foundation/index"
                target="_blank"
                >公益基金会</a
              >
            </dd>
          </dl>
          <dl class="col-links">
            <dt>特色服务</dt>
            <dd>
              <a rel="nofollow" href="//www.mi.com/order/fcode" target="_blank"
                >F 码通道</a
              >
            </dd>
            <dd>
              <a rel="nofollow" href="//www.mi.com/order/giftcode" target="_blank"
                >礼物码</a
              >
            </dd>
            <dd>
              <a rel="nofollow" href="//www.mi.com/service/imei" target="_blank"
                >防伪查询</a
              >
            </dd>
          </dl>
          <div class="col-contact">
            <p class="phone">400-100-5678</p>
            <p>8:00-18:00（仅收市话费）</p>
            <a rel="nofollow" class="btn btn-line-primary btn-small J_contactBtn"
              ><em class="iconfont-message2"></em> 人工客服
            </a>
            <div class="follow">
              关注小米：<a
                href="https://weibo.com/xiaomishangcheng"
                target="_blank"
                class="wb"
              ></a>
              <a
                @mouseover="show = 1"
                @mouseout="show = 0"
                href=""
                id="J_followWx"
                class="wx"
              ></a>
              <img
                src="//cdn.cnbj1.fds.api.mi-img.com/staticsfile/global/wx-img.png"
                id="J_followWxImg"
                v-show="show == 1"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="site-info">
        <div class="wrapper">
          <div class="logo ir">小米官网</div>
          <div class="info-text">
            <p class="sites">
              <a rel="nofollow" href="//www.mi.com/index.html" target="_blank"
                >小米商城</a
              >
              <span class="sep">|</span>
              <a rel="nofollow" href="//www.miui.com/" target="_blank">MIUI</a>
              <span class="sep">|</span>
              <a rel="nofollow" href="//home.mi.com/index.html" target="_blank"
                >米家</a
              >
              <span class="sep">|</span>
              <a rel="nofollow" href="http://www.miliao.com/" target="_blank"
                >米聊</a
              >
              <span class="sep">|</span>
              <a rel="nofollow" href="//www.duokan.com/" target="_blank"
                >多看</a
              >
              <span class="sep">|</span>
              <a rel="nofollow" href="//game.xiaomi.com/" target="_blank"
                >游戏</a
              >
              <span class="sep">|</span>
              <a
                rel="nofollow"
                href="//b.mi.com/?client_id=180100031058&amp;masid=17409.0358"
                target="_blank"
                >政企服务</a
              >
              <span class="sep">|</span>
              <a rel="nofollow" href="//xiaomi.tmall.com/" target="_blank"
                >小米天猫店</a
              >
              <span class="sep">|</span>
              <a
                rel="nofollow"
                href="//privacy.mi.com/all/zh_CN/"
                target="_blank"
                >小米集团隐私政策</a
              >
              <span class="sep">|</span>
              <a
                rel="nofollow"
                href="//cdn.cnbj1.fds.api.mi-img.com/mi-mall/f516fe9e2c01.html"
                target="_blank"
                >小米公司儿童信息保护规则</a
              >
              <span class="sep">|</span>
              <a
                rel="nofollow"
                href="//cdn.cnbj1.fds.api.mi-img.com/mi-mall/ded8d0e4a77d.html"
                target="_blank"
                >小米商城隐私政策</a
              >
              <span class="sep">|</span>
              <a
                rel="nofollow"
                href="//www.mi.com/about/user-agreement/"
                target="_blank"
                >小米商城用户协议</a
              >
              <span class="sep">|</span>
              <a rel="nofollow" href="//static.mi.com/feedback/" target="_blank"
                >问题反馈</a
              >
              <span class="sep">|</span>
              <a
                rel="nofollow"
                href="javascript:void(0);"
                class="J_siteGlobalRegion"
                >Select Location</a
              >
            </p>
            <p class="sites">
              <a rel="nofollow" href="http://www.mi.com/beihu" target="_blank"
                >北京互联网法院法律服务工作站</a
              >
              <span class="sep">|</span>
              <a rel="nofollow" href="http://www.cca.org.cn/" target="_blank"
                >中国消费者协会</a
              >
              <span class="sep">|</span>
              <a rel="nofollow" href="http://www.bj315.org/" target="_blank"
                >北京市消费者协会</a
              >
            </p>
            <p>
              ©
              <a href="javascript:;" target="_blank" title="mi.com">mi.com</a>
              京ICP证110507号
              <a href="http://beian.miit.gov.cn/" target="_blank" rel="nofollow"
                >京ICP备10046444号</a
              >
              <a
                rel="nofollow"
                href="http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=11010802020134"
                target="_blank"
                >京公网安备11010802020134号</a
              >
              <a href="//www.mi.com/culture-license/" target="_blank"
                >京网文[2020]0276-042号</a
              >
              <br />
              <a href="//www.mi.com/medical/record/" target="_blank"
                >（京）网械平台备字（2018）第00005号</a
              >
              <a href="//www.mi.com/medical/qualification/" target="_blank"
                >互联网药品信息服务资格证 (京)-非经营性-2014-0090</a
              >
              <a href="//www.mi.com/business-license/" target="_blank"
                >营业执照</a
              >
              <a href="//www.mi.com/medical/list/" target="_blank"
                >医疗器械质量公告</a
              >
              <br />
              <a
                href="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/e0c7d4cf3b7cd88de10196e30c92e020.png"
                target="_blank"
                >增值电信业务许可证</a
              >&nbsp;网络食品经营备案 京食药网食备202010048 &nbsp;
              <a
                href="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/c6859168166651511897f54fa1047fe3.png"
                target="_blank"
                >食品经营许可证</a
              >
              <br />
              违法和不良信息举报电话：171-5104-4404&nbsp;<a
                href="https://www.mi.com/intellectual"
                target="_blank"
                >知识产权侵权投诉</a
              >&nbsp;本网站所列数据，除特殊说明，所有数据均出自我司实验室测试
            </p>
          </div>
          <div class="info-links">
            <a
              rel="nofollow"
              href="//privacy.truste.com/privacy-seal/validation?rid=4fc28a8c-6822-4980-9c4b-9fdc69b94eb8&amp;lang=zh-cn"
              target="_blank"
              ><img
                rel="nofollow"
                src="//i1.mifile.cn/f/i/17/site/truste.png"
                alt="TRUSTe Privacy Certification"
            /></a>
            <a
              rel="nofollow"
              href="//search.szfw.org/cert/l/CX20120926001783002010"
              target="_blank"
              ><img
                rel="nofollow"
                src="//s01.mifile.cn/i/v-logo-2.png"
                alt="诚信网站"
            /></a>
            <a
              id="_xinchacharenzheng_cert_vip_kexinweb"
              rel="nofollow"
              href="//xyt.xinchacha.com/pcinfo?sn=523009637759455232&amp;certType=6"
              target="_blank"
              ><img
                rel="nofollow"
                src="//xyt.xinchacha.com/img/icon/icon3.png"
                alt="可信网站"
            /></a>
            <a
              rel="nofollow"
              href="//www.mi.com/service/buy/commitment/"
              target="_blank"
              ><img
                rel="nofollow"
                src="//i8.mifile.cn/b2c-mimall-media/ba10428a4f9495ac310fd0b5e0cf8370.png"
                alt="诚信经营 放心消费" /></a
            ><a
              rel="nofollow"
              href="https://webcert.cnmstl.net/cert/grade?sn=3af21034e35011eab3ea00163e068ceb"
              class="safe-auth J_safeAuth"
              ><img
                rel="nofollow"
                src="https://cnbj1.fds.api.xiaomi.com/b2c-misite-activity/f1ee261b96ae71e845efba398efeca02.png"
                class="img1" /><img
                rel="nofollow"
                src="https://cnbj1.fds.api.xiaomi.com/b2c-misite-activity/4e2aef5ae4711a6d7e8a10847d4544fe.png"
                class="img2"
            /></a>
          </div>
        </div>
        <div class="slogan ir">探索黑科技，小米为发烧而生</div>
    </div>
  </div>
</template>

<script>
import { ref } from "@vue/reactivity";
import { onMounted } from "@vue/runtime-core";
export default {
  name: "MiFooter",
  setup() {
    let show = ref(0);

    onMounted(() => {
      console.log("show的值：", show.value);
    });

    return { show };
  },
};
</script>

<style lang='scss' scoped>
a:hover {
  color: #ff6700;
}

.site-info .info-text .sites a:hover {
    color: #ff6700;
}

.site-info .info-text a:hover {
    color: #ff6700;
}

.mi-footer {
  background-color: #fff;
  &-service {
    display: grid;
    padding: 27px 0;
    grid-template-columns: repeat(5, 1fr);
    grid-auto-flow: column;
    border-bottom: 1px solid #e0e0e0;
    & a {
      color: #616161;
      text-align: center;
      font-size: 16px;
      line-height: 25px;
      border-left: 1px solid #e0e0e0;
      & em {
        margin-right: 6px;
        font-size: 24px;
        line-height: 24px;
        vertical-align: -4px;
      }
    }
  }
}

.footer-links {
  padding: 40px 0;
}

.footer-links .col-links {
  float: left;
  width: 160px;
  margin: 0;
}

.footer-links .col-links dt {
  margin: -1px 0 26px;
  font-size: 14px;
  line-height: 1.25;
  color: #424242;
}

.footer-links .col-links dd {
  margin: 10px 0 0;
  font-size: 12px;
}

.footer-links .col-links a {
  color: #757575;
  &:hover {
    color: #ff6700;
  }
}

.footer-links .col-contact {
  float: right;
  width: 251px;
  border-left: 1px solid #e0e0e0;
  text-align: center;
  color: #616161;
}

.footer-links .col-contact .phone {
  font-size: 22px;
  line-height: 1;
  color: #ff6700;
}

.footer-links .col-contact p {
  margin: 0 0 5px 0;
  font-size: 12px;
}

.site-footer .footer-links .col-contact .follow {
  font-size: 12px;
  margin-top: 10px;
  position: relative;
}

.site-footer .footer-links .col-contact .follow .wb {
  background: url(https://cdn.cnbj1.fds.api.mi-img.com/staticsfile/global/wb.png)
    50% 0 no-repeat;
  background-size: cover;
}

.footer-links .col-contact .follow .wx {
  background: url(https://cdn.cnbj1.fds.api.mi-img.com/staticsfile/global/wx.png)
    50% 0 no-repeat;
  background-size: cover;
}

.footer-links .col-contact .follow img {
  width: 126px;
  height: 126px;
  z-index: 2;
  position: absolute;
  top: 20px;
  left: 100px;
}

.btn {
  display: inline-block;
  width: 158px;
  height: 38px;
  padding: 0;
  margin: 0;
  border: 1px solid #b0b0b0;
  font-size: 14px;
  line-height: 38px;
  text-align: center;
  color: #b0b0b0;
  cursor: pointer;
  -webkit-transition: all 0.4s;
  transition: all 0.4s;
}

.btn-line-primary {
  border-color: #ff6700;
  background: #fff;
  color: #ff6700;
  &:hover {
    color: #fff;
    background-color: #f25807;
    border-color: #f25807;
  }
}

.btn-small {
  width: 118px;
  height: 28px;
  font-size: 12px;
  line-height: 28px;
}

.footer-links .col-contact .follow {
  font-size: 12px;
  margin-top: 10px;
  position: relative;
}

.footer-links .col-contact .follow .wb {
  background: url(https://cdn.cnbj1.fds.api.mi-img.com/staticsfile/global/wb.png)
    50% 0 no-repeat;
  background-size: cover;
  width: 24px;
  height: 24px;
  display: inline-block;
  vertical-align: middle;
  margin-left: 6px;
  margin-top: -3px;
  &:hover {
    background-image: url(https://cdn.cnbj1.fds.api.mi-img.com/staticsfile/global/wb@2x.png);
  }
}

.footer-links .col-contact .follow .wx {
  background: url(https://cdn.cnbj1.fds.api.mi-img.com/staticsfile/global/wx.png)
    50% 0 no-repeat;
  background-size: cover;
  width: 24px;
  height: 24px;
  display: inline-block;
  vertical-align: middle;
  margin-left: 6px;
  margin-top: -3px;
  &:hover {
    background-image: url(https://cdn.cnbj1.fds.api.mi-img.com/staticsfile/global/wx@2x.png);
  }
}

.footer-links {
  padding: 40px 0;
  height: 170px;
  box-sizing: content-box;
}

.site-info {
  padding: 30px 0;
  font-size: 12px;
  background: #fafafa;
}

.site-info .slogan {
    clear: both;
    margin: 30px auto 0;
    width: 100%;
    height: 19px;
    background: url(https://cdn.cnbj1.fds.api.mi-img.com/staticsfile/global/slogan2020.png) no-repeat center 0;
}

.site-info .logo {
    width: 56px;
    height: 56px;
    margin-right: 10px;
    background: url(//s02.mifile.cn/assets/static/image/logo-mi2.png) no-repeat;
    background-size: 56px;
    position: absolute;
    top: 0;
    left: 0;
}

.ir {
    display: block;
    text-align: left;
    text-indent: -9999em;
    overflow: hidden;
}

.site-info .info-text {
    color: #b0b0b0;
    padding-left: 67px;
}

.site-info .info-text p {
    margin: 0;
    line-height: 18px;
}

.site-info .info-text .sites a {
    color: #757575;
}

.site-info .info-text a {
    color: #b0b0b0;
}

.site-info .info-links {
    height: 28px;
    margin: 4px 0 15px;
    padding-left: 67px;
}

.site-info .info-links a {
    display: inline-block;
}

.site-info .info-links .safe-auth {
    width: 150px;
    height: 28px;
    overflow: hidden;
    margin-left: 5px;
    position: relative;
}

.site-info {
  padding: 30px 0;
  font-size: 12px;
  background: #fafafa;
}

.footer-links {
  padding: 40px 0;
}

.site-info .info-links img {
    width: auto;
    height: 28px;
    margin-left: 0;
}

a:hover {
  color: #ff6700;
}
</style>