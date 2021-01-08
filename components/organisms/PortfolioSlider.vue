<template>
<section class="portfolio" id="portfolio">
      <div class="contents-wrap">
        <div class="port-main-title">
          <h2>PORTFOLIO</h2>
        </div>
        <div class="port-contents">
          <swiper :options="swiperOption" class="port-contents-list">
            <swiper-slide class="port-contents-item">
              <img src="~/assets/images/fake.png" alt="">
              <p class="title">Twitter Clone</p>
              <p>2021.1.15</p>
              <p>Go,Gin,React,TypeScript</p>
            </swiper-slide>
            <swiper-slide class="port-contents-item">
              <img src="~/assets/images/AfterMountain.png" alt="">
              <p class="title">AfterMountain</p>
              <p>2020.6.15</p>
              <p>Ruby on Rails,React,TypeScript, AWS(S3,EC2)</p>
              <p>登山後に行きたい温泉が見つかる温泉×登山のメディア</p>
            </swiper-slide>
            <swiper-slide class="port-contents-item">
              <img src="~/assets/images/fake.png" alt="">
              <p class="title">Twitter Clone</p>
              <p>2001.1.15</p>
              <p>Go,Gin,React,TypeScript</p>
            </swiper-slide>
          </swiper>
        </div>
      </div>
      <div class="port-scroll-area">
        <p class="port-scroll-line"></p>
      </div>
    </section>
</template>

<script>
import { Swiper, SwiperSlide, directive } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'

export default {
    components: {
        Swiper,
        SwiperSlide
    },
    data(){
        return {
            swiperOption:{
                speed: 1000, //スライドの切り替わりスピード
                spaceBetween: 30, //各スライドの余白
                centeredSlides: true,//スライダーを真ん中に
                loop: true,  //無限ループ
                autoplay: {  //スライドの自動切り替え
                    delay: 5000, //スライドの自動切り替えの秒数
                    disableOnInteraction: false //何らかのアクション後の自動切り替えを再開
                }
            }
        }
    }
}
</script>

<style lang="scss">
.contents-wrap {
  max-width: 1440px;
  width: 90%;
  margin: 0 auto;
}

.port-main-title {
  text-align: right;
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
      animation: scrollLineLeft 2s ease infinite;
    }
  }
}
.port-contents{
  width: 100%;
  height: auto;
  &-list{
      width: 100%;
      height: auto;
      margin: 60px 0;
      pointer-events: none;
    }
  &-item {
      width: 30%;
      opacity: 0.7;
      img {
        width: 30%;
        opacity: 1;
    }
  }
}


section.portfolio {
  width: 100%;
  height: auto;
  padding: 180px 0;
  position: relative;
  background-color: rgba(58, 58, 58, 0.582);
}

.port-scroll-area {
  position: absolute;
  bottom: 70px;
  left:50%;
  transform: translate(-50%, -50%);
}

.port-scroll-line {
    width: 1px;
    height: 80px;
    background-color: rgb(136, 136, 136);
    position: absolute;
    left: 50%;
    top: 1.8em;

    &::before {
      content: '';
      display: block;
      width: 1px;
      height: 80px;
      background-color: rgb(255, 255, 255);
      animation: scrollLine 1.6s ease infinite;
      position: absolute;
      left: 0;
    }
}


@media screen and (max-width: 768px) {
.port-main-title {
    text-align: right;
    margin: 50px 0;
    h2 {
      font-size: 9.5vw;
      position: relative;
      &::after {
        content: "";
        display: block;
        position: absolute;
        width: 90%;
        height: 1px;
        background-color: #fff;
        animation: scrollLineLeft 2s ease infinite;
      }
    }
  }
  .port-contents {
    width: 100%;
    height: auto;
    ul {
      li {
        width: 100%;
        p.title {
          padding-top: 20px;
        }
        img {
          width: 90%;
        }
      }
    }
  }
}
</style>