<template>
  <div>
    <div class="logo">
      <img src="../static/GetPictureHvtThumbnailByPath-(2).png" alt />
    </div>
    <div class="lunbo">
      <img src="../static/联系.png" alt />
    </div>
    <div class="content">
      <div class="content1">
        <div class="techer">
          <img src="../static/老师.png" alt />
        </div>
        <div>
          <strong>李老师</strong>
          <p>信息工程学院</p>
        </div>
        <div class="phone">
          <img src="../static/电话.png" alt />
        </div>
      </div>
      <div class="content1">
        <div class="techer">
          <img src="../static/老师.png" alt />
        </div>
        <div>
          <strong>李老师</strong>
          <p>信息工程学院</p>
        </div>
        <div class="phone">
          <img src="../static/电话.png" alt />
        </div>
      </div>
      <div class="content1">
        <div class="techer">
          <img src="../static/老师.png" alt />
        </div>
        <div>
          <strong>李老师</strong>
          <p>信息工程学院</p>
        </div>
        <div class="phone">
          <img src="../static/电话.png" alt />
        </div>
      </div>
      <div class="content1">
        <div class="techer">
          <img src="../static/老师.png" alt />
        </div>
        <div>
          <strong>李老师</strong>
          <p>信息工程学院</p>
        </div>
        <div class="phone">
          <img src="../static/电话.png" alt />
        </div>
      </div>
      <div class="content1">
        <div class="techer">
          <img src="../static/老师.png" alt />
        </div>
        <div>
          <strong>李老师</strong>
          <p>信息工程学院</p>
        </div>
        <div class="phone">
          <img src="../static/电话.png" alt />
        </div>
      </div>
    </div>
    <!-- 联系我们 -->
    <div class="specialty">
      <div class="school">
        <map
          style="width: 343px; height: 222px;"
          :latitude="latitude"
          :longitude="longitude"
          :markers="covers"
        ></map>
        <strong>云南旅游职业学院</strong>
        <p>学校地址： 昆明市龙泉路268号</p>
        <p>联系电话： 0871-5187607 0871-5187890</p>
        <p>官方网址： http://zsw.ynctv.net/ http://www.ynctv.com/</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      id: 0, // 使用 marker点击事件 需要填写id
      title: "map",
      latitude: 25.075379,
      longitude: 102.711269,
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

.lunbo img {
  width: 375px;
  height: 160px;
}

.techer img {
  width: 73px;
  height: 73px;
}

.phone img {
  width: 53px;
  height: 28px;
}

.content {
  background: black;
  display: flex;
  flex-direction: column;
}
.content1 {
  display: flex;
  width: 100%;
  justify-content: space-around;
  align-items: center;
  background: #fff;
}

.specialty {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  margin: 40px 0px 60px 15px;
}

.specialty img {
  width: 150px;
  height: 102px;
}

.specialty p {
  font-size: 10px;
  text-align: center;
  color: #5e383d;
}

.specialty button {
  color: #7d1523;
  border: 1px solid #7d1523;
  border-radius: 0;
  font-size: 14px;
}

.school img {
  width: 343px;
  height: 164px;
}
.school strong {
  font-size: 18px;
  font-weight: 900;
  color: #515151;
  text-align: center;
  margin-bottom: 30px;
}

.school p {
  font-size: 14px;
  color: #515151;
  display: flex;
  flex-wrap: wrap;
}
</style>