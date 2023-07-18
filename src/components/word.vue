<template>
  <div class="word" :class="{ title: props.isTitle }">
    <ruby>
      {{ props.text }} <rp>(</rp><rt>{{ props.ruby }}</rt
      ><rp>)</rp>
    </ruby>
  </div>
</template>

<script setup lang="ts">
const props = defineProps({
  text: String,
  ruby: String,
  isTitle: Boolean,
});
</script>

<style scoped>
.word {
  display: inline-block;
  text-align: center;
  font-size: 26px;
  font-weight: bold;
  letter-spacing: 2px;
  color: #800000;
  padding: 2px;
}
.title {
  color: #333;
}
</style>
