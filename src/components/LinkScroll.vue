<template>
  <div id="linkscroll"
    :style="{ bottom: this.bottom + '%'}"
  >
    <a href="#">
      <div class=""
        :style="{ transform: 'rotate(' + this.angleComponent + 'deg)' }"
      >
        <svg version="1.1" id="Capa_1"
          xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
          x="0px" y="0px" width="20px" height="20px"
          viewBox="0 0 306 306" fill="#000"
          xml:space="preserve"
        >
          <g>
            <g id="expand-more">
              <polygon points="270.3,58.65 153,175.95 35.7,58.65 0,94.35 153,247.35 306,94.35"/>
            </g>
          </g>
        </svg>
      </div>
    </a>
  </div>
</template>

<script>
export default {
  name: 'LinkScroll',
  data () {
    return {
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
      let scroll = window.scrollY,
          percPosition = 0;
      percPosition = (100*scroll)/this.lengthPosition;
      this.angleComponent = (percPosition*180)/100;

      // console.log(percPosition);
      if (percPosition >= 95) {


        let y = percPosition; // 95 ~ 100



        let x = this.bottom - ((100-percPosition)/2);

        console.log(x);

        // this.bottom = 47.5;


      }
    }
  }
}
</script>

<style scoped lang="scss">
#linkscroll {
  position: absolute;
  // bottom: 50%;
  width: 100%;
  padding: 5px 0;
  cursor: pointer;
  z-index: 99;
}
</style>
