<template>
  <div>
    <h1 @click="counter.increment()">แผนการเรียน</h1>
    <h2>{{ counter.count }}</h2>
    <h2>{{ counter.doubleCount }}</h2>
    <h1>{{ news.newsList }}</h1>
  </div>
</template>
<script setup>
import { useCounterStore } from "@/stores/counter";
import { newsStore } from "@/stores/news";
const news = newsStore();
const counter = useCounterStore();
</script>
