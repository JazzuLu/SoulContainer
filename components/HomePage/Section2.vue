<template>
  <div ref="section" class="box">
    <div class=img_container>
      <img src="https://i.picsum.photos/id/497/1920/1080.jpg?hmac=lCmyuUeNJbmkWXfeLeQ2SxRu3mII34_GIdUIBn3M6RQ" alt=""/>
    </div>
    <div class="s2_content">
      <p>法庭上，辩护律师以“比利患有多重人格疾患，犯罪时神志不清，无法控制自己”为由，传召了4个精神病医生、一名心理学家上庭作证。</p>

      <p>经过长达2年的诉讼期，1979年，法庭宣判比利无罪。</p>

      <p>整个事件引起社会极大反响，各种攻击纷纷指向比利和精神专家。但宣判结果必有其庄严性，比利因此成为法律史上首个犯下重罪却因精神异常而获判无罪的人。</p>
    </div>
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
    gsap.to(this.$refs.section, {
      scrollTrigger: {
        trigger: this.$refs.section,
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
 .s2_content{
   font-size: 30px;color: #ffffff;z-index: 10;width: 65vw;margin: 10vh auto;
 }
</style>
