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
        <div class="prj-container">
          <div class="ordrslip" v-if="project === 'ordrslip'">
            <div class="container">
              <img src="../assets/ordrslip.png" alt="ordrslip site" class="ordrslip-img">
            </div>
            <div class="container proj-desc">
              <h1 class="title">OrdrSlip</h1>
              <p class="subtitle">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta, modi quis consequatur repellendus aspernatur, numquam autem vel dolor minus quo nemo facilis ad amet cupiditate alias beatae accusamus temporibus pariatur?</p>
            </div>
          </div>
          <div class="rose-sing" v-if="project === 'rose-sing'"></div>
          <div class="sixth-man" v-if="project === 'sixth-man'"></div>
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
    .prj-container {
      animation: fadeIn 3.5s;
    }
    .ordrslip {
      height: 100%;
      .container {
        display: flex;
        justify-content: center;
      }
      .proj-desc {
        flex-direction: column;
        width: 50%;
        padding: 10px;
        .title {
          color: #fff;
          font-weight: 300;
        }
        .subtitle {
          color: #fff;
          font-weight: 200;
        }
      }
      .ordrslip-img {
        height: 350px;
        border-radius: 15px;
        margin-bottom: 20px;
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
