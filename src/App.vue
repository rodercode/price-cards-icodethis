<script setup lang="ts">
import PriceCardList from "@/components/PriceCardList.vue";
import { ref } from "vue";

const cardInfoList = ref([
  {
    id: 1,
    title: "light",
    priceTag: "$19",
    maxConnections: 100,
    messagePerDay: "200,000",
    cardSize: "200px",
    btnColor: "is-success",
    headerColor: "has-text-success",
  },
  {
    id: 2,
    title: "startup",
    priceTag: "$49",
    maxConnections: 500,
    messagePerDay: "1 million",
    cardSize: "250px",
    btnColor: "is-primary",
    headerColor: "has-text-primary",
  },
  {
    id: 3,
    title: "big boy",
    priceTag: "$199",
    maxConnections: 5000,
    messagePerDay: "10 million",
    cardSize: "350px",
    btnColor: "is-info",
    headerColor: "has-text-info",
  },
]);
</script>

<template>
  <div class="container">
    <PriceCardList :cardInfoList="cardInfoList" />
  </div>
</template>

<style scoped>
@media screen and (max-width: 878px) {
  .container {
    padding: 32px 0px;
    flex-direction: column;
    justify-content: flex-start !important;
  }
}
.container {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 24px;
  height: 100vh;
}
</style>
