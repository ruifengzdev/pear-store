<script setup>
import { defineProps } from 'vue'

defineProps({
  imgUrl: String,
  text1: String,
  text2: String,
})

</script>

<template>
<div class="homepageFigure">
    <a href="/hammer-S1">
    <img :src="imgUrl">
    <div>
        <h1>{{ text1 }}</h1>
        <h2>{{ text2 }}</h2>
    </div>
    </a>
</div>
</template>

<style>
    .homepageFigure {
        width: 100%;
        background: black;
        color: white;
        margin: 0;
    }
    h1 {
        margin: 0;
        padding-top: 0.5em;
        color: white;
    }
    h2 {
        color: white;
    }
</style>