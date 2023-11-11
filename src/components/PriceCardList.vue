<script setup lang="ts">
import BaseCard from "./base/BaseCard.vue";
import { ref, inject } from "vue";
import type { CardInfo } from "../types/CardInfo";
const cardInfoList = inject("cardInfoList", ref<CardInfo[]>([]));
</script>

<template>
  <div v-for="cardInfo in cardInfoList" :key="cardInfo.id">
    <BaseCard :style="{ width: cardInfo.cardSize }" :cardInfo="cardInfo" />
  </div>
</template>
