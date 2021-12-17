<template>
  <div class="box orange">
    <div class="img_container">
      <img src="https://i.picsum.photos/id/410/1920/1080.jpg?hmac=WaY62swVOsVhkr0FVadjHuRxvjv0FULp1lQ-gQi-w-s" alt=""/>
    </div>
    <div class="label">Orange Panel</div>
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
    gsap.to(`.orange`, {
      scrollTrigger: {
        trigger: `.orange`,
        pin: true,
        scrub: 1,
        end: "bottom -100%",
      }
    });
    gsap.to(`.img_container`, {
      scrollTrigger: {
        trigger: `.orange`,
        scrub: 1,
        start: "top bottom",
        end: "bottom -300%",
      },
      scale:1.5,
      y: "-10%",
    });

  }
}
</script>

<style>
.orange{ background:#fc7f4e }

</style>
