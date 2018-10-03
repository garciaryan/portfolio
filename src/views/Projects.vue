<template>
  <div>
    <navBar />
    <div class="projects">
      <side-nav />
      <div class="prj">
        <div class="tabs is-toggle is-toggle-rounded is-centered">
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
                <span>Rose Sing</span>
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
              <img src="../assets/ordrslip.png" alt="ordrslip site" class="prj-img">
            </div>
            <div class="container proj-desc">
              <h1 class="title">OrdrSlip</h1>
              <p class="subtitle">OrdrSlip is a white-labeled food ordering app mainly focused on smaller businesses. There are many different applications that OrdrSlip is responsible for, and I built out the order flow for them all. Quesadilla Gorilla is the most popular one in Fresno, so download the app and check it out! Built in AngularJS and Ionic.</p>
            </div>
          </div>
          <div class="rose-sing" v-if="project === 'rose-sing'">
            <div class="container">
              <img src="../assets/rose-sing.png" alt="rose-sing site" class="prj-img">
            </div>
            <div class="container proj-desc">
              <h1 class="title">Rose Sing and Associates, Inc. - Electrical Consultants</h1>
              <p class="subtitle">Rose Sing is an electrical consulting agency based out of Visalia, CA. I designed and built their site using only HTML, CSS, and a handful of jQuery.</p>
            </div>
          </div>
          <div class="sixth-man" v-if="project === 'sixth-man'">
            <div class="container">
              <img src="../assets/sixth-man1.png" alt="sixth man app" class="sixth-man-img">
              <img src="../assets/sixth-man2.png" alt="sixth man app" class="sixth-man-img is-hidden-mobile">
            </div>
            <div class="container proj-desc">
              <h1 class="title">Sixth Man - Fantasy Basketball Helper</h1>
              <p class="subtitle">Sixth Man is a personal project that is currently unhosted. It's purpose is to search a database of players and rapidly compare their stats, all to aid in drafting and picking players up from the waiver wire. I built it in PHP and JavaScript using the Laravel and Vue frameworks.</p>
            </div>
          </div>
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
      .ordrslip, .rose-sing, .sixth-man {
        height: 100%;
      }
      .prj-img {
        height: 350px;
        border-radius: 15px;
        margin-bottom: 20px;
      }
      .sixth-man-img {
        height: 290px;
        margin-bottom: 20px;
        margin-right: 20px;
        border-radius: 15px;
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
  @media only screen and (max-width: 375px){
    .prj {
      .prj-container {
        .prj-img {
          height: 200px;
          border-radius: 0;
        }
        .sixth-man-img {
          height: 200px;
          border-radius: 0;
          margin-right: 0;
        }
        .proj-desc {
          width: 100%;
          padding: 20px;
        }
      }
    }
  } 
</style>
