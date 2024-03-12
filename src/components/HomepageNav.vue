<script>

</script>
<template>
<div class="outterBar">
    <div class="innerBar">
        <div class="col"><img class="col" src="https://cdn-image2.fengrin.me/xiandehuang%2F2018new_doge02_org.png" width="14px"></div>
        <div class="col">商店</div>
        <div class="col">锤</div>
        <div class="col">槌</div>
        <div class="col">改锥</div>
        <div class="col">螺丝</div>
        <div class="col">螺母</div>
        <div class="col">棒槌</div>
        <div class="col">工具箱</div>
        <div class="col">扳子</div>
        <div class="col">剪刀</div>
        <div class="col"><img src="https://cdn-image2.fengrin.me/xiandehuang%2Ffangdajing.png" width="14px"></div>
        <div class="col"><img src="https://cdn-image2.fengrin.me/xiandehuang%2Fbag.png" width="14px"></div>
    </div>
</div>
</template>
<style>
    .innerBar {
      display: grid;
      grid-template-columns: repeat(13, 1fr);
      grid-gap: 10px;
      background-color: rgb(20, 19, 19);
      width: 75%;
    }

    .col {
      padding: 10px;
      display: flex;
      align-items: center;
    }
    .outterBar {
        display: grid;
        place-items: center; /* 水平和垂直居中 */
        background-color: rgb(20, 19, 19);
        color: gray;
        font-size: 9pt;
    }
</style>