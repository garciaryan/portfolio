<template>
  <div>
    <navBar />
    <div class="projects">
      <side-nav />
      <div class="prj">
        <div class="tabs is-toggle is-medium is-centered">
          <ul>
            <li @click="project = 'ordrslip'" :class="{'is-active': project === 'ordrslip'}">
              <a>
                <span class="icon is-small"><i class="fal fa-utensils"></i></span>
                <span>OrdrSlip</span>
              </a>
            </li>
            <li @click="project = 'rose-sing'" :class="{'is-active': project === 'rose-sing'}">
              <a>
                <span class="icon is-small"><i class="fal fa-bolt"></i></span>
                <span>Rose Sing and Associates, Inc.</span>
              </a>
            </li>
            <li @click="project = 'sixth-man'" :class="{'is-active': project === 'sixth-man'}">
              <a>
                <span class="icon is-small"><i class="fal fa-basketball-ball"></i></span>
                <span>6th Man</span>
              </a>
            </li>
          </ul>
        </div>
        <div class="ordrslip" v-if="project === 'ordrslip'"></div>
        <div class="rose-sing" v-if="project === 'rose-sing'"></div>
        <div class="sixth-man" v-if="project === 'sixth-man'"></div>
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
  name: 'projects',
  components: {
    navBar,
    footerBar,
    sideNav
  },

  data () {
    return {
      project: 'ordrslip'
    }
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
    .tabs {
      padding-top: 20px;
      animation: fadeIn 3s;
      a {
        border-color: $whitePink;
        color: #fff;
        &:hover {
          background-color: #fff;
          border-color: $whitePink;
          color: $purple;
        }
      }
      li {
        &.is-active a{
          background-color: $whitePink;
          border-color: $whitePink;
          color: $purple;
        }
      }
    }
  }

  @keyframes slideLeft {
    from {width: 0vh;}
    to {width: 100%;}
  }
  @keyframes fadeIn {
    0% {opacity: 0;}
    66% {opacity: 0;}
    100% {opacity: 1;}
  }
</style>
