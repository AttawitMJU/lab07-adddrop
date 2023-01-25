<template>
  <div>
    <h1>Add Drop</h1>
    <h2>{{ counter.count }}</h2>
    <h2>{{ counter.doubleCount }}</h2>
  </div>
</template>
<script setup>
import { useCounterStore } from "@/stores/counter";
const counter = useCounterStore();
</script>
