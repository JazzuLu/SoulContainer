<template>
  <div class="box blue">
    <div class=img_container>
      <img src="https://i.picsum.photos/id/497/1920/1080.jpg?hmac=lCmyuUeNJbmkWXfeLeQ2SxRu3mII34_GIdUIBn3M6RQ" alt=""/>
    </div>
    <SplitText/>
  </div>
</template>

<script>

import gsap from "gsap";
import SplitText from "../BonusPluginTest/SplitText";

export default {
  components: {SplitText},
  props:{

  },
  data(){
    return {
    }
  },
  mounted() {
    gsap.to(`.blue`, {
      scrollTrigger: {
        trigger: `.blue`,
        start: "top top",
        end: "+=2000",
        pin: true,
        pinSpacing: false,
      }
    });
  }
}
</script>

<style>
.blue{ background:#36b6fc }

</style>
