<template>
  <div id="linkscroll">
    <a href="#work">
      Trabalhos
      <div class="">
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
}
</script>

<style scoped lang="scss">
#linkscroll {
  position: absolute;
  bottom: 50%;
  width: 100%;
  cursor: pointer;
}
</style>
