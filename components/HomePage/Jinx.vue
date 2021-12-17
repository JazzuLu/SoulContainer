<template>
  <div ref="contain" class="box">
    <div class="noise" style="position: absolute;width: 100vw;height: 100vh;"></div>
    <video style="width: 35vw;z-index: 10;" src="https://f.video.weibocdn.com/u0/SkN2Wn1rgx07SeJVKSru01041202oMk90E010.mp4?label=mp4_1080p&template=1444x812.25.0&trans_finger=0bde055d9aa01b9f6bc04ccac8f0b471&media_id=4715445891301499&tp=8x8A3El:YTkl0eM8&us=0&ori=1&bf=2&ot=h&ps=3lckmu&uid=2R4fOP&ab=3915-g1,6377-g0,1192-g0,1191-g0,1258-g0,3601-g15&Expires=1639737208&ssig=Ve1eYnHfGw&KID=unistore,video" controls="controls"></video>
    <div style="position: absolute;right: 0;bottom: 0;height: 100%;">
      <img style="height: 100%;" :src="jinx_1" alt="">
    </div>
  </div>
</template>

<script>

import gsap from "gsap";
import jinx_1 from "../../assets/img/roles/jinx_1.png"

export default {
  props:{

  },
  data(){
    return {
      jinx_1
    }
  },
  mounted() {
    // gsap.to(this.$refs.contain, {
    //   scrollTrigger: {
    //     trigger: this.$refs.contain,
    //     pin: true,
    //     scrub: 1,
    //     end: "bottom -100%",
    //   }
    // });
    // gsap.to(this.$refs.img_container, {
    //   scrollTrigger: {
    //     trigger: this.$refs.contain,
    //     scrub: 1,
    //     start: "top bottom",
    //     end: "bottom -300%",
    //   },
    //   scale:1.5,
    //   y: "-10%",
    // });
  }
}
</script>

<style>

</style>
