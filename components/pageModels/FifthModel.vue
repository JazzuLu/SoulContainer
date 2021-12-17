<template>
  <div class="box pink">
    <div class="img_container">
      <img src="https://picsum.photos/1920/1080?random=5" alt=""/>
    </div>
<!--    <div style="z-index: 2;">Pink Panel</div>-->
    <div class="svg_test">
      <MotionPathHelper/>
      <Physics2D/>
      <DrawSVG/>
      <MorphSVG/>
    </div>
  </div>
</template>

<script>
import MorphSVG from "../BonusPluginTest/MorphSVG";
import DrawSVG from "../BonusPluginTest/DrawSVG";
import Physics2D from "../BonusPluginTest/Physics2D";
import MotionPathHelper from "../BonusPluginTest/MotionPathHelper";
export default {
  components: {MotionPathHelper, Physics2D, DrawSVG, MorphSVG},
  props:{

  },
  data(){
    return {
    }
  },
  mounted() {

  }
}
</script>

<style scoped>
.pink{ background: #ef8b8b }
.svg_test{ width: 800px;max-height:60vh;margin: 15vh auto;z-index: 2;overflow-y:auto;overflow-x: hidden; }
</style>
