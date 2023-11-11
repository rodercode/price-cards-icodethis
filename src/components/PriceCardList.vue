<script setup lang="ts">
import BaseCard from "./base/BaseCard.vue";
import type { PropType } from "vue";
import type { CardInfo } from "../types/CardInfo";

const props = defineProps({
  cardInfoList: {
    type: Array as PropType<CardInfo[]>,
    required: true,
  },
});
</script>

<template>
  <BaseCard
    v-for="cardInfo in cardInfoList"
    :key="cardInfo.id"
    :style="{ width: cardInfo.cardSize }"
    :cardInfo="cardInfo"
  />
</template>
