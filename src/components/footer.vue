<template>
  <footer class="footer">
    <div class="content has-text-centered">
      <span class="name">rgarciadev<span class="copy">&copy;</span> front end development</span>
      <div class="address">
        <span>Fresno, CA</span>
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
  .name {
    font-weight: 400;

    .copy {
      font-weight: 300;
    }
  }

</style>
