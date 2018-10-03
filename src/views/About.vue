<template>
  <div>
    <navBar />
    <div class="about">
      <side-nav />
      <div class="tile is-ancestor">
        <div class="tile is-parent">
          <article class="tile is-child box left-tile">
            <img src="../assets/me.jpg" alt="profile pic">
          </article>
        </div>
        <div class="tile is-parent is-8">
          <article class="tile is-child box right-tile">
            <p class="title">Ryan Garcia</p>
            <p class="subtitle">Web and software developer </p>
            <div class="content">
              <p>
                I love building beautiful websites and applications. I also love basketball, playing music, and traveling.
              </p>
            </div>
          </article>
        </div>
      </div>
    </div>
    <footerBar />
  </div>
</template>

<script>
import navBar from '@/components/nav.vue'
import footerBar from '@/components/footer.vue'
import sideNav from '@/components/sideNav.vue'

export default {
  name: 'about',
  components: {
    footerBar,
    sideNav,
    navBar
  }
}
</script>

<style lang="scss" scoped>
@import "@/sass/styles.scss";
  .about {
    height: 100vh;
    position: relative;
    background-color: $washedLavender;
    animation: 1.5s slideRight;
  }
  .is-ancestor {
    align-items: center;
    height: inherit;
    animation: fadeIn 2.5s;
    width: 100%;
    margin-left: 0 !important;
    .box {
      &.right-tile {
        margin-right: 10vw !important;
      }
      &.left-tile {
        margin-left: 10vw !important;
      }
    }
  }

  @keyframes slideRight {
    from { width: 0vh; }
    to { width: 100%; }
  }
  @keyframes fadeIn {
    0% {opacity: 0;}
    66% {opacity: 0;}
    100% {opacity: 1;}  
  }
  @media only screen and (max-width: 375px){
    .is-ancestor {
      .box {
        &.right-tile {
          margin: 0 5vw !important;
        }
        &.left-tile {
          margin: 5vw 5vw 0 5vw !important;
        }
      }
    }
  }
</style>
