<template>
  <div>
    <navBar />
    <div class="home">
      <side-nav />
      <section class="hero left">
        <div class="hero-body"></div>
      </section>
      <section class="hero right">
        <div class="hero-body"></div>
      </section>
    </div>
    <footerBar />
  </div>
</template>

<script>
// @ is an alias to /src
import navBar from '@/components/nav.vue'
import footerBar from '@/components/footer.vue'
import sideNav from '@/components/sideNav.vue'

export default {
  name: 'home',
  components: {
    navBar,
    footerBar,
    sideNav
  }
}
</script>

<style lang="scss" scoped>
@import "@/sass/styles.scss";

  .home {
    display: flex;
    position: relative;
    min-height: calc(100vh - 192px);
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
  }

  @keyframes slideDown {
    from {
      height: 0vh;
    }
    to {
      height: 100%;
    }
  }
</style>
