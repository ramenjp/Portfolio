<template>
<header>
    <div class="pc_part">
      <h1 class="main-logo">Yosuke Takagi</h1>
      <nav>
        <ul class="flex">
          <li><a href="#about">ABOUT</a></li>
          <li><a href="#portfolio">PORTFOLIO</a></li>
          <li><a href="#contact">CONTACT</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
</script>

<style lang="scss">
header {
  width: 90%;
  margin: 0 auto;
  position: relative;
  z-index: 3;

  .main-logo {
    position: absolute;
    left: 0;
    top: 60px;
    
    img {
      width: 100%;
      height: auto;
    }

    /**  ロゴ画像 設定後　削除  **/
    font-size: 40px;
  }
  nav {
    position: absolute;
    top: 60px;
    right: 0;

    ul {
      li {
        padding-left: 40px;
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
</style>