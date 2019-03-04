<template>
  <section id="work">
    <div
      class="links-title"
      :style="{ opacity: this.opacity }"
    >Trabalhos:</div>
    <div class="link-items">

      <div class="links-work">
        <a href="http://www.eduardosparremberger.com.br/" target="_blank">
          <img src="../assets/works/eduardo-sparremberger.png" alt="">
          <p>Eduardo Sparremberger</p>
        </a>
      </div>
      <div class="links-work">
        <a href="http://www.equipevirtus.com.br/" target="_blank">
          <img src="../assets/works/virtus.png" alt="">
          <p>Equipe Virtus</p>
        </a>
      </div>
      <div class="links-work">
        <a href="http://www.mundoverdepaisagismo.com/" target="_blank">
          <img src="../assets/works/mundo-verde.png" alt="">
          <p>Mundo Verde Paisagismo</p>
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
  & .links-title {
    position: absolute;
    top: 6vh;
    font-size: 35px;
  }
  & .link-items {
    display: flex;
    align-items: center;
    & .links-work {
      position: relative;
      display: inline-block;
      margin: 15px 30px;
      & img {
        width: 100px;
      }
      & p {
        color: white;
        width: 100px;
      }
    }
  }
}
@media screen and (max-width: 500px) {
  #work {
    & .links-title {
      top: 4vh;
      font-size: 26px;
    }
    & .link-items {
      display: block;
      align-items: center;
      & p {
        font-size: 14px;
      }
    }
  }
}
</style>
