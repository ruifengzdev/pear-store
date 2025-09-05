<script setup>
import HomepageNav from './components/HomepageNav.vue'
import HomepageFigure from './components/HomepageFigure.vue'
import HomepageNewStore from './components/HomepageNewStore.vue';
</script>

<template>
  <HomepageNav />
  <div class="homepageHero">
    <HomepageFigure imgUrl="https://cdn-image2.ruifeng.me/xiandehuang%2Fhammer-S1.png" text1="Hammer pro" text2="得锤，敲敲打打，修葺一新"/>
  </div>
  <div class="homepageNewStore">
    <HomepageNewStore imgUrl="https://cdn-image2.ruifeng.me/xiandehuang/xiandehuang_marguerite-729510_1280.png" text1="Tool 火星" text2="2099 年"/>
  </div>
  <a href="mailto:inter18099#hotmail.com">Contact me</a>
</template>
<style>
.homepageHero {
  background-color: gray;
  width:100%;
  margin-bottom: 10px;
}
.homepageNewStore {
  background-color: gray;
  width:100%;
  margin-bottom: 10px;
}
</style>