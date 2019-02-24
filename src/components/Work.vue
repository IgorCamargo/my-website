<template>
  <section id="work">
    <div class="">
      <a href="#">
        <img src="../assets/logo.png" alt="">
      </a>
      <a href="#">
        <img src="../assets/logo.png" alt="">
      </a>
      <a href="#">
        <img src="../assets/logo.png" alt="">
      </a>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Work',
}
</script>

<style scoped lang="scss">
#work {
  background-color: darkred;
  display: flex;
  align-items: center;
  justify-content: center;
  & img {
    width: 100px;
    margin: 15px;
  }
}
</style>
