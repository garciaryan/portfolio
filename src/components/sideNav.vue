<template>
  <div class="side-nav is-hidden-mobile">
    <a href="https://github.com/garciaryan"><i class="fab fa-github"></i></a>
    <a href="https://www.linkedin.com/in/ryan-garcia-b98b66127/"><i class="fab fa-linkedin-in"></i></a>
    <a href="https://www.instagram.com/yetanotheryan/?hl=en"><i class="fab fa-instagram"></i></a>
    <a href="https://www.facebook.com/ryan.garcia.3705"><i class="fab fa-facebook-square"></i></a>
  </div>
</template>

<script>
export default {
  name: 'side-nav'
}
</script>

<style lang="scss" scoped>
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
    a {
      color: $purple;
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
