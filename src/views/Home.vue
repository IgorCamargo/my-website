<template>
  <div id="home">
    <Name msg="Igor Felipe de Camargo"/>
    <LinkScroll
      :bottom="bottom"
      :angleComponent="angleComponent"
    />
    <Work
      :percPosition="percPosition"
    />
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
  },
  data () {
    return {
      percPosition: 0,
      lengthPosition: 0,
      angleComponent: 0,
      bottom: 50,
    };
  },
  created () {
    let html = document.documentElement;
    this.lengthPosition = html.clientHeight;
  },
  mounted () {
    window.addEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      let scrolly = window.scrollY;

      this.percPosition = (100*scrolly)/this.lengthPosition;
      this.angleComponent = (this.percPosition*180)/100;
    }
  }
}
</script>

<style scoped lang="scss">
#home {
  position: relative;
  & #name, & #work {
    height: 100vh;
  }
}
</style>
