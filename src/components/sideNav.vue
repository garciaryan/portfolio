<template>
  <div class="side-nav is-hidden-mobile">
    <a href="https://github.com/garciaryan" target="_blank"><i class="fab fa-github"></i></a>
    <a href="https://www.linkedin.com/in/ryan-garcia-b98b66127/" target="_blank"><i class="fab fa-linkedin-in"></i></a>
    <a href="https://www.instagram.com/yetanotheryan/?hl=en" target="_blank"><i class="fab fa-instagram"></i></a>
    <a href="https://www.facebook.com/ryan.garcia.3705" target="_blank"><i class="fab fa-facebook-square"></i></a>
  </div>
</template>

<script>
export default {
  name: 'side-nav'
}
</script>

<style lang="scss">
@import "@/sass/styles.scss";
  .side-nav {
    position: fixed;
    width: 10vw;
    height: calc(100vh - 192px);
    display: flex;
    right: 0;
    flex-direction: column;
    justify-content: space-evenly;
    font-size: 25px;
    animation: 1.8s slideLeft;
    text-align: center;
    z-index: 9;
    a {
      color: lighten(#000, 20%);
      transition: all 0.2s ease-in-out;
      &:hover {
        transform: scale(1.8);
      }
    }
  }

  @keyframes slideLeft {
    from {
      left: 100%;
    }
    to {
      left: 90%;
    }
  }
</style>
