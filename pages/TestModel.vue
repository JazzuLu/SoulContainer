<template>
  <div class="container">
<!--    <FirstModel/>-->
<!--    <SecondModel/>-->
<!--    <ThirdModel/>-->
<!--    <FourthModel/>-->
<!--    <FifthModel/>-->
<!--    <Section4/>-->
    <Physics2D/>
  </div>
</template>

<script>
import FirstModel from "../components/pageModels/FirstModel";
import SecondModel from "../components/pageModels/SecondModel";
import ThirdModel from "../components/pageModels/ThirdModel";
import FourthModel from "../components/pageModels/FourthModel";
import FifthModel from "../components/pageModels/FifthModel";
import Section4 from "../components/HomePage/Section4";
import MorphSVG from "../components/BonusPluginTest/MorphSVG";
import Physics2D from "../components/BonusPluginTest/Physics2D";

export default {
  components:{
    Physics2D,
    MorphSVG,
    Section4,
    FifthModel,
    FourthModel,
    ThirdModel,
    SecondModel,
    FirstModel,
  },
  mounted() {
    // console.log($)

  }
}
</script>
<style>
</style>
