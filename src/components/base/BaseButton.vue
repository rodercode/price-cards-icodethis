<script setup lang="ts">
const props = defineProps({
  mode: String,
});
</script>
<template>
  <button :class="'button' + ' ' + mode">
    <slot> </slot>
  </button>
</template>

<style lang="css" scoped>
.button:hover {
  color: #343a40;
  font-weight: 700;
}
</style>
