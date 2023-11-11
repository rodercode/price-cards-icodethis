<script setup lang="ts">
import type { PropType } from "vue";
import type { CardInfo } from "@/types/CardInfo";
import BaseButton from "./BaseButton.vue";

const props = defineProps({
  cardInfo: {
    type: Object as PropType<CardInfo>,
    required: true,
  },
});
</script>
<template>
  <div class="card">
    <div class="card-content">
      <div class="content has-text-centered">
        <header class="has-background-grey-lighter">
          <h1
            class="title has-text-white is-uppercase mb-0"
            :class="cardInfo.headerColor"
          >
            {{ cardInfo.title }}
          </h1>
        </header>
        <main>
          <span class="price-value">{{ cardInfo.priceTag }}</span>
          <ul>
            <li>
              <span class="subtitle">{{ cardInfo.maxConnections }}</span>
              <span>Max Connections</span>
            </li>
            <li>
              <span class="subtitle">{{ cardInfo.messagePerDay }}</span>
              <span>Messages Per Day</span>
            </li>
            <li>
              <span class="subtitle">Encryption</span>
              <span>SSL Protection</span>
            </li>
          </ul>
          <div class="my-5">
            <BaseButton
              :mode="'is-uppercase is-medium' + ' ' + cardInfo.btnColor"
            >
              <p>Select Plan</p>
            </BaseButton>
          </div>
        </main>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
span {
  display: block;
}

header {
  padding: 16px;
  display: flex;
  justify-content: center;
  margin-bottom: 64px;
}
.price-value {
  font-size: 60px;
  display: block;
  margin-bottom: 24px;
}
ul {
  display: flex;
  flex-direction: column;
  gap: 16px;
  margin: 0;
  list-style: none;
}

.subtitle {
  font-weight: 700;
  margin: 0;
  color: #343a40;
}

@media screen and (max-width: 878px) {
  .card {
    width: 280px !important;
  }
}
</style>
