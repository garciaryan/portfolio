<template>
  <footer class="footer">
    <div class="content columns is-mobile">
      <div class="column logo-col">
        <img src="../assets/logo.svg" alt="logo" class="logo">
      </div>
      <div class="column">
        <span class="name">rgarciadev<span class="copy">&copy;</span> front end development</span>
        <div class="address">
          <span>Fresno, CA</span>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'footerBar'
}
</script>

<style lang="scss" scoped>
@import "@/sass/styles.scss";
  .footer {
    height: 15vh;
  }
  .name {
    font-weight: 400;

    .copy {
      font-weight: 300;
    }
  }
  .logo-col {
    justify-content: flex-end;
    display: flex;
    .logo {
      height: 50px;
    }
  }

</style>
