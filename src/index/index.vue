
<template>
  <div>
    <div class="logo">
      <img src="../static/GetPictureHvtThumbnailByPath-(2).png" alt />
    </div>
    <swiper
      class="swiper"
      :indicator-dots="indicatorDots"
      :autoplay="autoplay"
      :interval="interval"
      :duration="duration"
    >
      <swiper-item v-for="(item,index) in imgList" :key="{index}">
        <view class="swiper-item">
          <img :src="imgurl+item.url" alt />
        </view>
      </swiper-item>
    </swiper>
    <!-- 选项按钮 -->
    <div class="xx">
      <navigator url="../index/xuexiaogaikuo" open-type="switchTab" hover-class="none">
        <div class="xuanxiang">
          <img src="../static/学校概况2.png" alt />
          <p>学校概括</p>
        </div>
      </navigator>
      <navigator url="../index/zoujinlvyuan" open-type="switchTab" hover-class="none">
        <div class="xuanxiang">
          <img src="../static/特色专业.png" alt />
          <p>特色专业</p>
        </div>
      </navigator>
      <navigator url="../index/zhaoshengjianzhang" open-type="switchTab" hover-class="none">
        <div class="xuanxiang">
          <img src="../static/招生简章2.png" alt />
          <p>招生简章</p>
        </div>
      </navigator>
      <navigator url="../index/baomingzixun" open-type="switchTab" hover-class="none">
        <div class="xuanxiang">
          <img src="../static/phones.png" alt />
          <p>联系我们</p>
        </div>
      </navigator>
    </div>

    <!-- 特色专业 -->
    <div class="title">
      <h1>特色专业</h1>
      <p>characteristics of professional</p>
      <div class="specialty">
        <div>
          <img src="../static/院系设置.png" alt />
          <p>宝玉石鉴定与加工</p>
        </div>
        <div>
          <img src="../static/工程测量.png" alt />
          <p>工程测量技术</p>
        </div>
        <div>
          <img src="../static/升学就业.png" alt />
          <p>高速铁路客运乘务</p>
        </div>
        <div>
          <img src="../static/奖励体系.png" alt />
          <p>空中乘务</p>
        </div>
        <button>查看更多</button>
      </div>
    </div>
    <!-- 走进旅院 -->
    <div class="title">
      <h1>走进旅院</h1>
      <p>welcome to tourism vocation</p>
      <div class="specialty">
        <div>
          <img src="../static/院系设置.png" alt />
          <p>院系设置</p>
        </div>
        <div>
          <img src="../static/名师风采.png" alt />
          <p>名师风采</p>
        </div>
        <div>
          <img src="../static/升学就业.png" alt />
          <p>升学就业</p>
        </div>
        <div>
          <img src="../static/奖励体系.png" alt />
          <p>奖励体系</p>
        </div>
        <navigator url="../index/zoujinlvyuan" open-type="switchTab" hover-class="none">
          <button>查看更多</button>
        </navigator>
      </div>
    </div>
    <!-- 学校概括 -->
    <div class="title baoming">
      <h1>学校概括</h1>
      <p>School profile</p>
      <div class="specialty">
        <div class="school">
          <img src="../static/timg (2).png" alt />
          <p>
            这里是学校简介，大约展示三行文字左右，超出的部分用…三点省略号代替
            这里大约也就能写三行
            或者四行
          </p>
        </div>
        <navigator url="../index/xuexiaogaikuo" open-type="switchTab" hover-class="none">
          <button>详细了解我们</button>
        </navigator>
      </div>
    </div>

    <!-- 招生计划 -->
    <div class="title">
      <h1>招生计划</h1>
      <p>The adminssion plan</p>
      <div class="specialty plan_p">
        <p>2020年招生计划</p>
        <div class="school plan">
          <img src="../static/8de904b7c48ed38988907484824f28f2.png" alt />
          <div class="span">
            <span class="span1">云南旅游职业学院计划2020年招生…</span>
            <span class="span2">2020-06-15. 15:53:45</span>
          </div>
        </div>
        <navigator url="../index/zhaoshengjianzhang" open-type="switchTab" hover-class="none">
          <button>查看更多</button>
        </navigator>
      </div>
    </div>

    <!-- 报名咨询 -->
    <div class="title baoming">
      <h1>报名咨询</h1>
      <p>Registration consulting</p>
      <div class="specialty plan_p">
        <p>报名咨询</p>
        <div class="school plan">
          <div class="span">
            <span>请报名学子及时查看小程序内最新招生信息，如有疑问，可以点击下方联系电话或手机进行咨询！</span>
            <span class="span2">2020-06-17 11:50:10</span>
          </div>
        </div>
        <navigator url="../index/baomingzixun" open-type="switchTab" hover-class="none">
          <button>查看更多</button>
        </navigator>
      </div>
    </div>

    <!-- 联系我们 -->
    <div class="title">
      <h1>联系我们</h1>
      <p>Contact us</p>
      <div class="specialty">
        <map
          style="width: 343px; height: 222px;"
          :latitude="latitude"
          :longitude="longitude"
          :markers="covers"
        ></map>
        <div class="school" :src="texturl+item.url">
          <!-- <strong :src="texturl+item.url">云南旅游职业学院</strong>
          <p :src="texturl+item.url">学校地址： 昆明市龙泉路268号</p>
          <p :src="texturl+item.url">联系电话： 0871-5187607 0871-5187890</p>
          <p :src="texturl+item.url">官方网址： http://zsw.ynctv.net/ http://www.ynctv.com/</p> -->
        </div>
        <navigator url="../index/baomingzixun" open-type="switchTab" hover-class="none">
          <button>查看更多</button>
        </navigator>
      </div>
    </div>
  </div>
</template>

<script>
import { url } from "../util/comm";
export default {
  data() {
    return {
      indicatorDots: true,
      autoplay: true,
      interval: 3000,
      duration: 500,
      imgurl: url,
      texturl: url,
      id: 0, // 使用 marker点击事件 需要填写id
      title: "map",
      latitude: 25.075379,
      longitude: 102.711269,
      imgList: [],
      text: [],
      covers: [
        {
          latitude: 25.075379,
          longitude: 102.711269,
          iconPath: "../static/position.png",
        },
        {
          latitude: 25.075379,
          longitude: 102.711269,
          iconPath: "../static/position.png",
        },
      ],
    };
  },
  onLoad() {
    console.log(url);
    uni.request({
      url: url + "api/services/app/MiniProgramCarousel/GetCarousels", 
      data: {},
      method: "GET",
      header: {
        "Content-Type": "application/x-www-form-urlencoded",
      },
      success: (res) => {
        this.imgList = res.data.result;
      },
    });

    uni.request({
      url: url + "api/services/app/MiniProgramArticle/GetConsultation",
      data: {
        // name: "测试",
        // address: "昆明市北市区",
        // longitude: 25.075362,
        // latitude: 102.711301,
        // contactNumber: "42000000",
        // webSite: "1234658888",
      },
      method: "GET",
      header: {
        "Content-Type": "application/x-www-form-urlencoded",
      },
      success: (res) => {
        this.text = res.data.result;
      },
    });
  },
};
</script>

<style>
.logo {
  width: 60%;
  height: 50px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: center;
}
.logo img {
  width: 107px;
  height: 25px;
}
.swiper-item img {
  width: 100%;
  height: 160px;
}

/* 选项按钮 */
.xx {
  display: flex;
  width: 100%;
  justify-content: space-around;
  align-items: center;
  margin: 20px 0 10px 0;
}

.xuanxiang img {
  width: 40px;
  height: 40px;
}
.xuanxiang p {
  font-size: 12px;
  font-family: "PingFangSC-Medium";
}

/* 特色专业 */
.title {
  text-align: center;
  margin-top: 20px;
  margin-bottom: 40px;
}

.title h1 {
  font-size: 24px;
  color: #7d1523;
}

.title p {
  font-size: 12px;
  color: #b2b2b2;
  margin-bottom: 20px;
}
.specialty {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.specialty img {
  width: 150px;
  height: 102px;
}

.specialty p {
  font-size: 12px;
  text-align: center;
  color: #5e383d;
}

.specialty button {
  color: #7d1523;
  border: 1px solid #7d1523;
  border-radius: 0;
  font-size: 14px;
}

/* 学校概括*/
.school img {
  width: 343px;
  height: 164px;
}

.school p {
  font-size: 14px;
  color: #515151;
  display: flex;
  flex-wrap: wrap;
}

/* 招生计划 */
.plan_p {
  width: 95%;
  margin: 0 auto;
}

.plan_p p {
  font-size: 18px;
  font-weight: 900;
  color: #515151;
  text-align: left;
}
.plan img {
  width: 129px;
  height: 80px;
}

.plan {
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.span span {
  color: #515151;
}
.span1 {
  font-size: 14px;
}

.span2 {
  font-size: 12px;
}

/* 报名咨询 */
.baoming {
  background: #f5f5f5;
}

.baoming .span .span2 {
  font-size: 10px;
}

.school strong {
  font-size: 18px;
  font-weight: 900;
  color: #515151;
}
</style>