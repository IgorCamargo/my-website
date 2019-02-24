<template>
  <div id="home">
    <Name msg="Igor Felipe de Camargo"/>
    <LinkScroll/>
    <Work/>
  </div>
</template>

<script>
// @ is an alias to /src
import Name from '@/components/Name.vue'
import LinkScroll from '@/components/LinkScroll.vue'
import Work from '@/components/Work.vue'

export default {
  name: 'home',
  components: {
    Name,
    LinkScroll,
    Work,
  }
}
</script>

<style scoped lang="scss">
#home {
  position: relative;
  // width: 100vw;
  // height: 100vh;
  // display: flex;
  // align-items: center;
  // justify-content: center;
  & #name, & #work {
    height: 100vh;
  }
}
</style>
