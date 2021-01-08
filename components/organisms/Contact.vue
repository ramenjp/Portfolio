<template>
<section class="contact" id="contact">
      <div class="con-main-title">
        <h2>CONTACT</h2>
      </div>
      <p class="con-text">お仕事のご相談や、ご不明点などあれば以下のメールアドレスにお送りください。</p>
      <div class="contact-button">
        <a href="mailto:takagiyousuke5@gmail.com">Direct Mail</a>
      </div>
      <div class="scroll-up">
        <a href="#top"><img src="~/assets/images/scroll-up.png" alt=""></a>
      </div>
</section>
</template>

<script>

</script>

<style lang="scss">
section.contact {
  width: 90%;
  height: auto;
  padding: 60px 0;
  margin: 180px auto;
  background-color: rgba(82, 82, 82, 0.384);
  position: relative;
}
.scroll-up {
  position: absolute;
  bottom: -60px;
  right: 50px;
  transition: .4s;
  img {
    width: 26px;
    height: 84px;
  }
  &:hover {
    transform: translateY(-15px);
  }
}
.con-main-title {
  text-align: center;
  h2 {
    font-size: 70px;
  }
}
p.con-text {
  padding: 30px 0;
  text-align: center;
}
.contact-button {
  width: 440px;
  height: 160px;
  line-height: 160px;
  background-color: #7B7B7B35;
  margin: 40px auto;
  transition: all .4s;
  a {
    text-align: center;
    display: block;
    width: 100%;
    height: 100%;
    color: #fff;
  }
  &:hover {
    background-color: rgb(100, 100, 100);
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
@media screen and (max-width: 768px) {
section.contact {
    width: 100%;
    height: auto;
    padding: 60px 0;
    margin: 180px auto;
    position: relative;
  }
  .scroll-up {
    position: absolute;
    bottom: -60px;
    right: 50px;
    transition: 0.4s;
    img {
      width: 26px;
      height: 84px;
    }
    &:hover {
      transform: translateY(-15px);
    }
  }
.con-main-title {
    text-align: center;
    h2 {
      font-size: 9.5vw;
    }
  }
  p.con-text {
    padding: 30px 0;
    text-align: center;
  }
  .contact-button {
    width: 280px;
    height: 120px;
    line-height: 120px;
  }
}
</style>
