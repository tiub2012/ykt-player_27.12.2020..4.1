<template>
  <div id="ykt-wrapper" :style="{height, width}">
    ykt-player_4.1
    {{test}}
  </div>
</template>

<script>
import { mapGetters } from "vuex";

export default {
  data: () => ({
    height: '',
    width: ''
  }),
  methods:{
    updateSize() {
      this.height = `${document.documentElement.clientHeight}px`
      this.width = `${document.documentElement.clientWidth}px`
      console.log(this.height, this.width)
    }
  },
  mounted(){
    this.height = `${document.documentElement.clientHeight}px`
    this.width = `${document.documentElement.clientWidth}px`
  },
  created() {
    window.addEventListener("resize", this.updateSize);
  },
  name: "YKT-PLAYER"
};
</script>

<style>
#ykt {
  position: relative;
}
</style>
