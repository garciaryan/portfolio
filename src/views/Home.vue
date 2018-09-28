<template>
  <div>
    <navBar />
    <div class="home">

    </div>
    <footerBar />
  </div>
</template>

<script>
// @ is an alias to /src
import navBar from '@/components/nav.vue'
import footerBar from '@/components/footer.vue'

export default {
  name: 'home',
  components: {
    navBar,
    footerBar
  }
}
</script>

<style lang="scss" scoped>
@import "@/sass/styles.scss";

  .home {
    height: 100vh;
    position: relative;
    top: 18px;
    background-color: $whitePink;
  }
</style>
