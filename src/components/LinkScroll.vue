<template>
  <div id="linkscroll"
    :style="{ bottom: this.bottom + '%'}"
  >
    <a href="#work">
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
  props: ['angleComponent', 'bottom'],
}
</script>

<style scoped lang="scss">
#linkscroll {
  position: absolute;
  width: 100%;
  padding: 5px 0;
  cursor: pointer;
  z-index: 99;
}
</style>
