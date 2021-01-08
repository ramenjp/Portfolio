<template>
 <section class="about" id="about">
      <div class="contents-wrap">
        <div class="ab-main-title">
          <h2>ABOUT</h2>
        </div>
        <div class="about-contents flex">
          <div class="left-contents"><img src="~/assets/images/left-img.png" alt=""></div>
          <div class="right-contents">
            <h3>Yosuke Takagi</h3>
            <p>1996/6/23 (Age: 24) </p>
            <p>Software Engineer</p>
            <div class="profile-skill">
            <h3>言語</h3>
              <ul class="profile-skill-list">
                <li><img src="~/assets/svg/React.svg" class="profile-skill-item"></li>
                <li><img src="~/assets/svg/Redux.svg" class="profile-skill-item"></li>
                <li><img src="~/assets/svg/Vue.svg" class="profile-skill-item"></li>
                <li><img src="~/assets/svg/Nuxt.svg" class="profile-skill-item"></li>
                <li><img src="~/assets/svg/Typescript.svg" class="profile-skill-item"></li>
                <li><img src="~/assets/svg/Go.svg" class="profile-skill-item"></li>
              </ul>
              <h3>その他ツール</h3>
              <ul class="profile-skill-list">
                <li><img src="~/assets/svg/Github.svg" class="profile-skill-item"></li>
                <li><img src="~/assets/svg/CircleCI.svg" class="profile-skill-item"></li>
                <li><img src="~/assets/svg/GoogleAnalytics.svg" class="profile-skill-item"></li>
                <li><img src="~/assets/svg/Contentful.svg" class="profile-skill-item"></li>
              </ul>
            </div>
          </div>
        </div>
      <div class="history">
        <h3>経歴</h3>
        <ul>
          <li>
            <div class="date">2020.5 ~</div>
            <p>株式会社HRBrainでフロントエンドエンジニアとして従事。</p>
          </li>
          <li>
            <div class="date">2019.4 ~ 2020.5</div>
            <p>楽天株式会社に新卒入社後、楽天モバイルネットワーク部署に配属。RFエンジニアとして関西全域の電波品質管理を行う。</p>
          </li>
          <li>
            <div class="date">~2019.3</div>
            <p>知識情報処理研究室にて、自然言語処理を用いた食品情報のネガポジ判定し、食品の評価・嗜好情報の分析する研究を行う。</p>
          </li>
        </ul>
      </div>
    </div>
      <div class="about-scroll-area">
        <p class="about-scroll-line"></p>
      </div>
    </section>
</template>

<script>
export default {}
</script>

<style lang="scss">
.contents-wrap {
  max-width: 1440px;
  width: 90%;
  margin: 0 auto;
}

.ab-main-title {
  margin: 50px 0;
  h2 {
    font-size: 70px;
    position: relative;
    &::after {
      content: '';
      display: block;
      position: absolute;
      width: 90%;
      height: 1px;
      background-color: #fff;
      animation: scrollLineRight 2s ease infinite;
    }
  }
}

.about-contents {
  width: 100%;
  height: auto;
  margin: 60px 0;
  justify-content: space-between;
}


.left-contents {
  width: 35%;
  img {
    width: 100%;
    height: auto;
  }
}

.right-contents {
  width: 60%;

  h3 {
    font-size: 24px;
  }
  p {
    font-size: 18px;
    padding: 10px 0;
  }
}

.profile-skill {
  padding: 20px 0;
  &-list {
    display:flex;
    margin-bottom:10px;
  }
  &-item {
      width:100px;
      height:100px;
      margin-right:30px;
  }
}

.history {
  width: 100%;
  height: auto;
  h3 {
    font-size: 24px;
    font-weight: bold;
  }
  ul {
    margin: 20px 0;
    li {
      padding: 20px 0;
      border-bottom: 1px solid #fff;

      .date {
        font-size: 20px;
        padding: 10px 0;
      }
    }
  }
}

@media screen and (min-width: 1025px) {
  .pc_part {
    display: block;
  }
  .sp_part {
    display: none;
  }
}

@media screen and (min-width: 769px) and (max-width: 1024px) {
  .pc_part {
    display: block;
  }
  .sp_part {
    display: none;
  }
}

@media screen and (max-width: 768px) {
  .pc_part {
    display: none;
  }
  .sp_part {
    display: block;
  }
}
</style>