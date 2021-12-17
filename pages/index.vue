<template>
  <div class="home container">
    <BannerTop/>
    <TransitionTitModel title="Section 1 ------ 犯罪 · 被捕"/>
    <Section1/>
    <TransitionTitModel title="Section 2 ------ 无罪 · 释放"/>
    <Section2/>
    <TransitionTitModel title="Section 3 ------ 真相 · 浮现"/>
    <Section3/>
    <TransitionTitModel title="Section 4 ------ 灵魂 · 容器"/>
    <Section4/>
    <TransitionTitModel title="Section 5 ------ 多重 · 人格"/>
    <Section5/>
    <TransitionTitModel title="Section 6 ------ Jinx · jinx"/>
    <Jinx/>
    <img :src="jinx_1" alt="">
  </div>
</template>

<script>

import jinx_1 from "../assets/img/roles/jinx_1.png"
import BannerTop from "../components/HomePage/BannerTop";
import FirstModel from "../components/pageModels/FirstModel";
import TransitionTitModel from "../components/commonModels/TransitionTitModel";
import Section1 from "../components/HomePage/Section1";
import Section2 from "../components/HomePage/Section2";
import Section3 from "../components/HomePage/Section3";
import Section4 from "../components/HomePage/Section4";
import Jinx from "../components/HomePage/Jinx";
import Section5 from "../components/HomePage/Section5";

export default {
  components:{
    Section5,
    Jinx,
    Section4,
    Section3,
    Section2,
    Section1,
    TransitionTitModel,
    FirstModel,
    BannerTop,
  },
  data:()=>({
    jinx_1
  }),
  mounted() {
    // console.log($)

  }
}
</script>
<style>
body{ background: #222; color: #ffffff;}
</style>
