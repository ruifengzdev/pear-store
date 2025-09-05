<script setup>
import { defineProps } from 'vue'

defineProps({
  imgUrl: String,
  text1: String,
  text2: String,
  text3: String,
  text4: String,
})

</script>

<template>
<div class="homepageFigure">
    <a href="/hammer-S1">
    <div>
        <h1>{{ text1 }}</h1>
        <h2>{{ text2 }}</h2>
    </div>
    <div class="img-container">
        <img :src="imgUrl" class="rotate-image">
    </div>
    </a>
</div>
</template>

<style>
    .homepageFigure {
        width: 100%;
        color: white;
        margin: 0;
        display: grid;
        place-items: center; /* 水平和垂直居中 */
    }
    h1 {
        margin: 0;
        padding-top: 0.5em;
        color: white;
    }
    h2 {
        color: white;
    }
    .img-container {
        width: 20rem; /* 设置容器宽度 */
        height: 20rem; /* 设置容器高度 */
        position: relative;
    }
    .rotate-image {
        width: 100%; /* 设置图片宽度 */
        height: 100%; /* 设置图片高度 */
        position: absolute;
        top: 0;
        left: 0;
        animation: rotateAnimation 4s linear; /* 旋转动画 */
        animation-fill-mode: forwards; /* 动画结束后保持最后状态 */
    }

    @keyframes rotateAnimation {
    from {
        transform: rotate(0deg); /* 开始时的旋转角度 */
    }
    to {
        transform: rotate(360deg); /* 结束时的旋转角度 */
    }
}
</style>