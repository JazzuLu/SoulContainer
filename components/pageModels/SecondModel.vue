<template>
  <div class="box green" style="height:300px">
    <div class="green_mask"/>
    <div class="img_container">
      <img src="https://i.picsum.photos/id/1033/1920/1080.jpg?hmac=PFeRtI5OXUqS7PbTPluUptCJV9_ZF4s_kN3P6teC8dI" alt=""/>
    </div>
    <div class="label">Green Panel</div>
  </div>
</template>

<script>

import gsap from "gsap";

export default {
  props:{

  },
  data(){
    return {
    }
  },
  mounted() {

    gsap.to(`.green .img_container`, {
      scrollTrigger: {
        trigger: `.green`,
        start: "top bottom",
        scrub:1,
        // end: "+=2000",
        // pin: true,
        // pinSpacing: false,
      },
      y:-600
    });
  }
}
</script>

<style>
.green{ background:#93d079 }
.green_mask{  z-index:100; box-shadow: 0 0 30px 2px #000 inset; position: absolute; width:100%;height:100%; top:0;left:0; }
</style>
