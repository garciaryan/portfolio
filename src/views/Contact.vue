<template>
  <div>
    <navBar />
    <div class="contact">
      <side-nav />
      <div class="form-container columns is-desktop">
        <div class="header-col">
          <h1 class="header">let's work together</h1>
        </div>
        <div class="container column">
          <form action="https://formspree.io/ryan@rgarciadev.com" method="POST" @submit="checkForm">

            <div class="field">
              <label class="label">Email</label>
              <div class="control has-icons-left has-icons-right">
                <input class="input" :class="{'is-danger': errors['Email required.']}" type="email" name="email" placeholder="hi@gmail.com" v-model="email">
                <input type="hidden" name="_next" value="/home" />
                <input type="hidden" name="_subject" value="New submission!" />
                <span class="icon is-small is-left">
                  <i class="fas fa-envelope"></i>
                </span>
                <span v-if="errors['Email required.']" class="icon is-small is-right">
                  <i class="fas fa-exclamation-triangle"></i>
                </span>
              </div>
              <p v-if="errors['Email required.']" class="help is-danger">This field is required.</p>
            </div>

            <div class="field">
              <label class="label">Message</label>
              <div class="control">
                <textarea class="textarea" placeholder="What's up?" name="message" :class="{'is-danger': errors['Message required.']}" v-model="message"></textarea>
                <span v-if="errors['Message required.']" class="icon is-small is-right">
                  <i class="fas fa-exclamation-triangle"></i>
                </span>
                <p v-if="errors['Message required.']" class="help is-danger">This field is required.</p>
              </div>
            </div>

            <div class="field is-grouped">
              <div class="control">
                <button class="button is-link" type="submit">Submit</button>
              </div>
            </div>
          </form>
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
  },

  data () {
    return {
      errors: [],
      email: null,
      message: null
    }
  },

  methods: {
    checkForm (e) {
      if (this.email && this.message) {
        return true
      }
      
      this.errors = []
      if (!this.email) this.errors.push('Email required.')
      if (!this.message) this.errors.push('Message required.')

      e.preventDefault()
    }
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
  justify-content: center;
  .button.is-link {
    background-color: $purple;
    
    &:hover {
      background-color: lighten($purple, 20%);
    }
  }
  .header-col {
    margin-right: 10px;
  }
  .header {
    text-align: center;
    font-size: 35px;
    font-weight: 300;
  }
  .container {
    width: 100%;
    form {
      width: 100%;
    }
  }
  .form-container {
    width: 80%;
    animation: fadeIn 2.2s;
    display: flex;
    align-items: center;
  }
}
@keyframes slideUp {
  from { margin-top: 100%; }
  to { margin-top: 0; }
}
@keyframes fadeIn {
  0% {opacity: 0;}
  66% {opacity: 0;}
  100% {opacity: 1;}
}
@media only screen and (max-width: 375px){
  .contact {
    .form-container {
      flex-direction: column;
      .header-col {
        display: flex;
        align-items: center;
        padding: 0;
        height: 33%;
        margin-right: 0;
      }
    }
  }
}
</style>
