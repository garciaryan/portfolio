<template>
  <div>
    <navBar />
    <div class="contact">
      <side-nav />
      <h1 class="header">let's work together</h1>
      <div class="container">
        <div class="field">
          <label class="label">Name</label>
          <div class="control">
            <input class="input" type="text" placeholder="Text input">
          </div>
        </div>

        <div class="field">
          <label class="label">Email</label>
          <div class="control has-icons-left has-icons-right">
            <input class="input is-danger" type="email" placeholder="Email input" value="hello@">
            <span class="icon is-small is-left">
              <i class="fas fa-envelope"></i>
            </span>
            <span class="icon is-small is-right">
              <i class="fas fa-exclamation-triangle"></i>
            </span>
          </div>
          <p class="help is-danger">This email is invalid</p>
        </div>

        <div class="field">
          <label class="label">Message</label>
          <div class="control">
            <textarea class="textarea" placeholder="Textarea"></textarea>
          </div>
        </div>

        <div class="field is-grouped">
          <div class="control">
            <button class="button is-link">Submit</button>
          </div>
          <div class="control">
            <button class="button is-text">Cancel</button>
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
  name: 'contact',
  components: {
    navBar,
    sideNav,
    footerBar
  }
}
</script>

<style lang="scss" scoped>
@import "@/sass/styles.scss";
.contact {
  height: 100vh;
  background-color: $lavender;
  animation: 1.5s slideUp;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  .header {
    text-align: center;
    font-size: 35px;
    font-weight: 300;
  }
  .container {
    width: 75%;
  }
}
@keyframes slideUp {
  from { margin-top: 100%; }
  to { margin-top: 0; }
}
</style>
