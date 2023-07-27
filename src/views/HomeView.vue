<template>
  <div class="count">{{ storeCounter.count }}</div>
  <div class="count">{{ storeCounter.doubleCount }}</div>
  <div class="buttons">
    <button @click="storeCounter.decrement" type="button">-</button>
    <button @click="storeCounter.increment" type="button">+</button>
  </div>
  <input type="number" v-model="storeCounter.count" />
</template>

<script setup>
import { useCounterStore } from "@/stores/counter";

const storeCounter = useCounterStore();
</script>
