<template>
  <section id="name">
    <div class="content-name">
      <p>
        {{ msg }}
      </p>
      <div class="link-contact">
        <a href="https://github.com/IgorCamargo" target="_blank">
          github.com/IgorCamargo
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Name',
  props: {
    msg: String
  }
}
</script>

<style scoped lang="scss">
#name {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: white;
  & .content-name {
    & p {
      font-size: 42px;
    }
    & .link-contact {
      & a {
        color: #555;
      }
      & :before {
        content: url('../assets/GitHub-16px.png');
        padding: 5px 8px;
        display: inline-block;
        vertical-align: middle;
      }
    }
  }
}
@media screen and (max-width: 500px) {
  #name {
    & .content-name {
      & p {
        font-size: 26px;
      }
    }
  }
}
</style>
