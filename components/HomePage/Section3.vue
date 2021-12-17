<template>
  <div ref="contain" class="box">
    <div class="img_container" ref="img_container">
      <img src="https://i.picsum.photos/id/410/1920/1080.jpg?hmac=WaY62swVOsVhkr0FVadjHuRxvjv0FULp1lQ-gQi-w-s" alt=""/>
    </div>
    <div class="content">

      <a href="https://baike.baidu.com/tashuo/browse/content?id=a079f3de4569ff20d7a44bd2&lemmaId=58830&fromLemmaModule=pcBottom&lemmaTitle=24%E4%B8%AA%E6%AF%94%E5%88%A9">24 billy</a>

      比利自8岁起，多次被继父殴打、威胁和强奸，有严重的精神疾患。在这悲惨的成长经历下，比利既想一死了之，又渴望能逃离这里继续生存，两种情绪反反复复，使得比利的内心不断分裂出新的人格。

      16岁时，比利自杀未遂，从此，原本的比利就被其他人格“保护”了起来，一沉睡就是7年，经审查和医学判定，他至少拥有24个不同的人格。
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

</style>
