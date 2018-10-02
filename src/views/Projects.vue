<template>
  <div>
    <navBar />
    <div class="projects">
      <side-nav />
      <div class="prj"></div>
    </div>
    <footerBar />
  </div>
</template>

<script>
import navBar from '@/components/nav.vue'
import footerBar from '@/components/footer.vue'
import sideNav from '@/components/sideNav.vue'

export default {
  name: 'projects',
  components: {
    navBar,
    footerBar,
    sideNav,
  }
}
</script>

<style lang="scss" scoped>
@import "@/sass/styles.scss";
  .projects {
    height: 100vh;
    width: 100%;
  }
  .prj {
    position: absolute;
    right: 0;
    background-color: $darkPink;
    animation: 1.5s slideLeft;
    height: inherit;
    width: 100%;
  }

  @keyframes slideLeft {
    from {width: 0vh;}
    to {width: 100%;}
  }
</style>
