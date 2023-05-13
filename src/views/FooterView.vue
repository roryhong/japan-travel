<template>
  <footer>
    <img class="fixed-image" src="../assets/images/富士山2.jpg" />
    <h3>追蹤我們</h3>
    <section class="links">
      <a href="#">
        <img
          title="facebook"
          src="../assets/Icons/facebook.svg"
          alt="facebook"
        />
      </a>
      <a href="#">
        <img
          title="instagram"
          src="../assets/Icons/instagram.svg"
          alt="instagram"
        />
      </a>
      <a href="#">
        <img title="twitter" src="../assets/Icons/twitter.svg" alt="twitter" />
      </a>
      <a href="#">
        <img title="youtube" src="../assets/Icons/youtube.svg" alt="youtube" />
      </a>
    </section>
  </footer>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
footer {
  display: flex;
  padding: 5rem;
  flex-direction: column;
  align-items: center;
  color: #fff;
  background-color: rgba(0, 0, 0, 0.5);

  .fixed-image {
    min-height: 100vh;
    position: fixed;
    width: 100%;
    z-index: -5;
    bottom: 0;
    left: 0;
  }

  .links {
    margin-top: 2rem;
    a {
      img {
        width: 5vh;
        margin: 0rem 1rem;
      }
    }
  }
}
</style>
