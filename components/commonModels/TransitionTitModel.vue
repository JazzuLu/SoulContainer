<template>
  <div ref="transitionTit" class="box transition_tit" style="height:300px">
    <div class="transition_tit_mask"/>
    <div class="img_container">
      <img src="https://i.picsum.photos/id/1033/1920/1080.jpg?hmac=PFeRtI5OXUqS7PbTPluUptCJV9_ZF4s_kN3P6teC8dI" alt=""/>
    </div>
    <div class="label">
      <span class="tit"></span><InputCursor/>
    </div>
  </div>
</template>

<script>

import gsap from "gsap";
import $ from "jquery"
import InputCursor from "../InputCursor";

export default {
  components: {InputCursor},
  props:{
    title:{type:String,default:"Section 1"}
  },
  data(){
    return {

    }
  },
  mounted() {

    gsap.to($(this.$refs.transitionTit).find(".img_container")[0], {
      scrollTrigger: {
        // trigger: `.transition_tit`,
        trigger: this.$refs.transitionTit,
        start: "top bottom",
        scrub:1,
        // end: "+=2000",
        // pin: true,
        // pinSpacing: false,
      },
      y:-600
    });

    gsap.to($(this.$refs.transitionTit).find(".label .tit")[0],{
      duration: 6,
      text: {
        value: this.title,
      },
      delay: 1,
    });
  }
}
</script>

<style>
.transition_tit{ background:#93d079 }
.transition_tit_mask{  z-index:100; box-shadow: 0 0 30px 2px #000 inset; position: absolute; width:100%;height:100%; top:0;left:0; }
</style>
