<template>
<footer>
    <div class="footer-contents">
      <nav>
        <ul class="flex">
          <li><a href="#about">ABOUT</a></li>
          <li><a href="#portfolio">PORTFOLIO</a></li>
          <li><a href="#contact">CONTACT</a></li>
        </ul>
      </nav>
      <div class="copyright">&copy; 2021 All Rights Reserved.</div>
    </div>
  </footer>
</template>


<script>
export default {}
</script>

<style lang="scss">
footer {
  width: 100%;
  height: auto;

  .footer-contents {
    text-align: center;

    nav {
      margin: 80px 0;
      ul {
        justify-content: center;
        li {
          padding-right: 40px;
        }
      }
    }
  }

.copyright {
      padding: 30px 0;
      color: #fff;
    }
}

.flex {
  display: flex;
}


</style>