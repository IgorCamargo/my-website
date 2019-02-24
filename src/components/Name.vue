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
  background-color: yellow;
  display: flex;
  align-items: center;
  justify-content: center;
  .content-name {
    p {
      font-size: 42px;
    }
    .link-contact {
      // background-color: #eee;
      a {
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
</style>
