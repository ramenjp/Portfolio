<template>
<div class="wrapper">
   <BackgroundCircle />
   <BackgroundGradation />
    <Header/>
    <div class="pc_part">
    <section class="main-visual">
      <div class="contents-wrap">
        <div class="main-text">
          <h2 class="fade-in hide">MY PORTFOLIO</h2>
          <p class="fade-in hide">Software Engineer</p>
        </div>
      </div>
      <div class="scroll-area">
        <p class="scroll-text">Scroll Down</p>
        <p class="scroll-line"></p>
      </div>
    </section>
    <History />   
    <PortfolioSlider />
    <Contact />
    <Footer />
  </div>
</div>
</template>

<script>
export default {
    mounted() {
        this.animation()
    },
    methods: {
        animation(){
            const fadeIn = document.querySelectorAll('.fade-in');
            const wrapper = document.querySelector('wrapper');
            setTimeout(function() {
                wrapper.classList.remove('flash');
            }, 400);
            
            for(let i = 0; i < fadeIn.length; i++) {
                setTimeout(function () {
                    fadeIn[0].classList.remove('hide');
                }, 800);
                setTimeout(function () {
                fadeIn[1].classList.remove('hide');
            }, 1400);
          }
        }
    }
}
</script>

<style lang="scss">
a {
  color: unset;
  text-decoration: none;
}
.flex {
  display: flex;
}
body {
  background-color: #242424;
  font-family: 'Merriweather', serif;
  transition: all 1s;
}
li {
  list-style-type: none;
}
.contents-wrap {
  max-width: 1440px;
  width: 90%;
  margin: 0 auto;
}
h1, h2, h3, p, li {
  line-height: 1.6;
  letter-spacing: .08em;
  color: #fff;
}

section.main-visual {
  width: 100%;
  height: 100vh;

  .main-text {
    position: absolute;
    top: 35%;
  }
  h2 {
    font-size: 70px;
  }
  p {
    font-size: 36px;
    padding-top: 30px;
  }
}

.scroll-area {
  position: absolute;
  bottom: 60px;
  left:50%;
  transform: translate(-50%, -50%);
  z-index: 2;

  p.scroll-text {
    font-size: 17px;
    position: relative;
  }
  p.scroll-line {
    width: 1px;
    height: 160px;
    background-color: rgb(136, 136, 136);
    position: absolute;
    left: 50%;
    top: 1.8em;

    &::before {
      content: '';
      display: block;
      width: 1px;
      height: 160px;
      background-color: rgb(255, 255, 255);
      animation: scrollLine 1.6s ease infinite;
      position: absolute;
      left: 0;
    }
  }
}

section.about {
  width: 100%;
  height: auto;
  background-color: rgba(75, 75, 75, 0.678);
  padding: 180px 0 220px;
  position: relative;
}
.about-scroll-area {
  position: absolute;
  bottom: 70px;
  left:50%;
  transform: translate(-50%, -50%);

  p.about-scroll-line {
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
  section.main-visual {
    width: 100%;
    height: 100vh;
    position: relative;
    .main-text {
      top: 40%;
    }
    h2 {
      font-size: 8.5vw;
    }
    p {
      font-size: 4.5vw;
      padding-top: 20px;
    }
  }
  .scroll-area {
    position: absolute;
    bottom: 40px;

    p.scroll-text {
      font-size: 14px;
    }
    p.scroll-line {
      height: 90px;
      top: 3em;

      &::before {
        height: 90px;
      }
    }
  }

  section.about {
    width: 100%;
    height: auto;
    padding: 180px 0 220px;
    position: relative;
  }
  .about-scroll-area {
    position: absolute;
    bottom: 70px;
    left: 50%;
    transform: translate(-50%, -50%);

    p.about-scroll-line {
      width: 1px;
      height: 80px;
      background-color: rgb(136, 136, 136);
      position: absolute;
      left: 50%;
      top: 1.8em;

      &::before {
        content: "";
        display: block;
        width: 1px;
        height: 80px;
        background-color: rgb(255, 255, 255);
        animation: scrollLine 1.6s ease infinite;
        position: absolute;
        left: 0;
      }
    }
  }

  .ab-main-title {
    h2 {
      font-size: 9.5vw;
    }
  }

  .about-contents {
    width: 100%;
    height: auto;
    margin: 60px 0;
    display: block;
  }
  .left-contents {
    width: 100%;
    img {
      width: 100%;
    }
  }
  .right-contents {
    width: 100%;

    h3 {
      padding-top: 20px;
      font-size: 24px;
    }
    p {
      font-size: 18px;
      padding: 10px 0;
    }
  }
  .profile-text {
    padding: 10px 0;
    p {
      font-size: 18px;
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
      margin: 10px 0;
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

  section.portfolio {
    width: 100%;
    height: auto;
    padding: 180px 0;
    position: relative;
  }
  .port-scroll-area {
    position: absolute;
    bottom: 70px;
    left: 50%;
    transform: translate(-50%, -50%);

    p.port-scroll-line {
      width: 1px;
      height: 80px;
      background-color: rgb(136, 136, 136);
      position: absolute;
      left: 50%;
      top: 1.8em;

      &::before {
        content: "";
        display: block;
        width: 1px;
        height: 80px;
        background-color: rgb(255, 255, 255);
        animation: scrollLine 1.6s ease infinite;
        position: absolute;
        left: 0;
      }
    }
  }
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
      button {
        display: none !important;
      }
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


/**   文字フェードイン    **/
.hide {
  opacity: 0;
}
.show {
  opacity: 1;
}
.fade-in {
  transition: all 1s;
}
.flash {
  opacity: 0;
}

@keyframes scrollLine {
    0% {
      height: 0;
      bottom: 100%;
    }
    50% {
      height: 100%;
      bottom: 0;
    }
    100% {
      height: 0;
      bottom: 0;
    }
  }
  
  @keyframes scrollLineRight {
    0% {
      width: 0;
      right: 100%;
    }
    50% {
      width: 100%;
      right: 0;
    }
    100% {
      width: 0;
      right: 0;
    }
  }
  
  @keyframes scrollLineLeft {
    0% {
      width: 0;
      left: 100%;
    }
    50% {
      width: 100%;
      left: 0;
    }
    100% {
      width: 0;
      left: 0;
    }
  }
</style>
