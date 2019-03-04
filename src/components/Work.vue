<template>
  <section id="work">
    <h1
      :style="{ opacity: this.opacity }"
    >Trabalhos:</h1>
    <div class="">

      <div class="links-work">
        <a href="#">
          <img src="../assets/logo.png" alt="">
          <p>Lorem Ipsum</p>
        </a>
      </div>
      <div class="links-work">
        <a href="#">
          <img src="../assets/logo.png" alt="">
          <p>Lorem Ipsum</p>
        </a>
      </div>
      <div class="links-work">
        <a href="#">
          <img src="../assets/logo.png" alt="">
          <p>Lorem Ipsum</p>
        </a>
      </div>

    </div>
  </section>
</template>

<script>
export default {
  name: 'Work',
  props: ['percPosition'],
  data () {
    return {
      opacity: 0,
    }
  },
  watch: {
    percPosition: function () {
      this.opacity = this.percPosition / 100;
    }
  }
}
</script>

<style scoped lang="scss">
#work {
  position: relative;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  & h1 {
    position: absolute;
    top: 6vh;
    font-size: 35px;
  }
  & .links-work {
    position: relative;
    display: inline-block;
    margin: 15px 30px;
    & img {
      width: 100px;
    }
    & p {
      color: white;
    }
  }
}
</style>
