<template>
  <div ref="contain" class="box">
    <div ref="img_container" class="img_container">
      <img src="https://i.picsum.photos/id/270/1920/1080.jpg?hmac=7AG21ARfiXrlnEVXCYC3OWyrGS9pdFPyCnLW7WzRTHw" alt=""/>
    </div>
    <div class="side_tit">宛平南路600号</div>
    <div class="content" style="font-size: 20px;">
      <p>精神分裂症是一组病因未明的慢性疾病，多在青壮年缓慢或亚急性起病，临床上往往表现为症状各异的综合征，涉及感知觉、思维、情感和行为等多方面的障碍以及精神活动的不协调。</p>
      <p>患者一般意识清楚，智能基本正常，但部分患者在疾病过程中会出现认知功能的损害。</p>
      <p>病程一般迁延，呈反复发作、加重或恶化，部分患者最终出现衰退和精神残疾，但有的患者经过药物治疗与心理治疗后可保持痊愈或基本痊愈状态。</p>
    </div>
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
    gsap.to(this.$refs.contain, {
      scrollTrigger: {
        trigger: this.$refs.contain,
        pin: true,
        scrub: 1,
        end: "bottom -100%",
      }
    });
    gsap.to(this.$refs.img_container, {
      scrollTrigger: {
        trigger: this.$refs.contain,
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
  .side_tit{font-size: 100px}
</style>
