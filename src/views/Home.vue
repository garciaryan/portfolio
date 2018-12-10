<template>
  <div>
    <navBar />
    <div class="home">
      <side-nav />
      <div class="images">
        <div class="img1">
          <img class="pres-img" src="../assets/presenting.jpg" alt="me, presenting an app">
        </div>
      </div>
      <section class="hero left">
        <div class="hero-body"></div>
      </section>
      <section class="hero right">
        <div class="hero-body"></div>
      </section>
      <div class="left-text">
        <h1>a website for </h1>
      </div>
      <div class="right-text">
        <vue-typed-js 
          :strings="['your business', 'your hobby', 'your startup', 'a friend', 'you']"
          :fadeOutDelay="1500"
          :typeSpeed="75"
          :fadeOut="true"
          :showCursor="false"
          :loop="true">
          <h1 class="typing"></h1>
        </vue-typed-js>
      </div>
    </div>
    <footerBar />
  </div>
</template>

<script>
// @ is an alias to /src
import navBar from '@/components/nav.vue'
import footerBar from '@/components/footer.vue'
import sideNav from '@/components/sideNav.vue'
import { VueTypedJs } from 'vue-typed-js'

export default {
  name: 'home',
  components: {
    navBar,
    footerBar,
    sideNav,
    VueTypedJs
  }
}
</script>

<style lang="scss" scoped>
@import "@/sass/styles.scss";

  .home {
    display: flex;
    position: relative;
    min-height: calc(100vh - 70px);
    .hero {
      width: 50%;
      position: absolute;
      z-index: -1;
      .hero-body {
        padding: 0;
        display: flex;
        align-items: center;
        justify-content: center;
      }
    }
    .left {
      background-color: $whitePink;
      height: 100%;
      left: 0;
      animation: 1.5s slideDown;
    }
    .right {
      background-color: $pink;
      height: 100%;
      right: 0;
      bottom: 0;
      animation: 1.5s slideDown;
    }
    .images {
      .img1 {
        .pres-img {
          padding: 10px;
          width: 210px;
          position: absolute;
        }
      }
    }
    .left-text {
      width: 50%;
      display: flex;
      justify-content: flex-end;
      align-items: center;
      h1 {
        font-size: 2.2em;
        font-weight: 300;
        padding-right: 5px;
        animation: fadeInText 2.5s;
      }
    }
    .right-text {
      width: 50%;
      display: flex;
      align-items: center;
      h1 {
        font-size: 2.2em;
        font-weight: 300;
        padding-left: 5px;
        animation: fadeInText 3s;
      }
    }
  }

  @keyframes slideDown {
    from {
      height: 0vh;
    }
    to {
      height: 100%;
    }
  }

  @keyframes fadeInText {
    0% { opacity: 0; }
    66% { opacity: 0; }
    100% { opacity: 1 }
  }
  @media only screen and (max-width: 375px){
    .home {
      .left-text {
        h1 {
          font-size: 2em;
        }
      }
      .right-text {
        h1 {
          font-size: 2em;
        }
      }
    }
  }
</style>
