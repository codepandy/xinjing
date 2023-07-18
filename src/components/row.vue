<template>
  <div class="row-container" :class="{ 'text-center': props.isTitle }">
    <section>
      <word
        v-for="(item, i) in textList"
        :text="item"
        :ruby="rubyList[i]"
        :isTitle="props.isTitle"
      />
    </section>
    <section class="explain">{{ props.explain }}</section>
  </div>
</template>

<script setup lang="ts">
import { computed } from "vue";
import word from "./word.vue";
const props = defineProps({
  text: { type: String, required: true },
  ruby: { type: String, required: true },
  explain: String,
  isTitle: Boolean,
});
const textList = computed(() => props.text.split(""));
const rubyList = computed(() => props.ruby.split(" "));
</script>

<style scoped>
.row-container {
  margin-top: 16px;
}
.text-center {
  text-align: center;
}
.explain {
  text-align: left;
}
</style>
