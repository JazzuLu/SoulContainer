<template>
  <div ref="section" class="box" style="height: 150vh;align-items: flex-start">
    <div class=img_container>
      <img src="https://i.picsum.photos/id/782/1920/1080.jpg?hmac=Yr45CXIjIidR5E6u-36gZ9BCbVCSUaBrZM1vhuBklgY" alt=""/>
    </div>
    <div class="content s2_content">
      <div style="margin-top: -50px;">

        汤姆（Tommy）（逃脱） / 戴维（David）（8岁） / 亚伦（Allen）（健谈）（右撇子）（告诉一切）  / 亚瑟（Arthur）（绅士）（英国腔）（控制所有人） / 里根（Ragen）
        <p>法庭上，辩护律师以“比利患有多重人格疾患，犯罪时神志不清，无法控制自己”为由，传召了4个精神病医生、一名心理学家上庭作证。</p>

        <p>经过长达2年的诉讼期，1979年，法庭宣判比利无罪。</p>

        <p>整个事件引起社会极大反响，各种攻击纷纷指向比利和精神专家。但宣判结果必有其庄严性，比利因此成为法律史上首个犯下重罪却因精神异常而获判无罪的人。</p>

        36岁 回归社会 / 54岁 被采访 / 2014 年遗逝
      </div>
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
.box .s2_content{ font-size: 42px;height: 100vh;display: flex;align-items: center; }
</style>
