<template>
  <div>
    <div class="logo">
      <img src="../static/GetPictureHvtThumbnailByPath-(2).png" alt />
    </div>
    <div class="lunbo">
      <img src="../static/走进旅院2.png" alt />
    </div>
    <div class="button">
      <img src="../static/Search Glyph.png" alt />
      <input type="text" placeholder="搜索.." />
      <button>取消</button>
    </div>
    <div class="picture">
      <div class="picture_1">
        <div class="picture_2">
          <img src="../static/院系设置.png" alt />
          <p>院系设置</p>
        </div>
        <div class="picture_2">
          <img src="../static/名师风采.png" alt />
          <p>名师风采</p>
        </div>
      </div>
      <div class="picture_1">
        <div class="picture_2">
          <img src="../static/升学就业.png" alt />
          <p>校园活动</p>
        </div>
        <div class="picture_2">
          <img src="../static/体系.png" alt />
          <p>奖励体系</p>
        </div>
      </div>
      <div class="picture_1">
        <div class="picture_2">
          <img src="../static/校园风景.png" alt />
          <p>校园风景</p>
        </div>
        <div class="picture_2">
          <img src="../static/奖励体系.png" alt />
          <p>食宿交通</p>
        </div>
      </div>
      <div class="picture_1">
        <div class="picture_2">
          <img src="../static/升学就业.png" alt />
          <p>可添加新的风景</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
/* logo */
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

.button {
  display: flex;
  justify-content: space-around;
}

.button img {
  width: 30px;
  height: 30px;
}

.button input {
  width: 265px;
  height: 29px;
  border: 1px solid #f5f5f5;
  background: #f5f5f5;
}

.button button {
  background: #7d1522;
  color: #fff;
  width: 66px;
  /* height: 29px; */
  border-radius: 50px;
  font-size: 14px;
}

/* 内容图片 */
.picture {
  background: #f5f5f5;
  width: 100%;
  margin-top: 50px;
  margin-bottom: 80px;
}

.picture_1 {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  margin: 20px 0 10px 0;
  text-align: center;
}

.picture_2 {
  background: #fff;
}
.picture img {
  width: 164px;
  height: 102px;
}

.picture_2 p {
  color: #5e383d;
  font-size: 12px;
}
</style>