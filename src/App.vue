<script setup>
import { ref } from "vue";
import { Motion, Presence } from "motion/vue";

const show = ref(true);
</script>

<template>
  <Presence>
    <Motion
      v-show="show"
      :initial="{ opacity: 0, scale: 0 }"
      :animate="{ opacity: 1, scale: 1 }"
      :exit="{ opacity: 0, scale: 0.6 }"
      class="box"
    />
  </Presence>
  <button @click="show = !show">show</button>
</template>

<style>
div {
  width: 100px;
  height: 100px;
  border-radius: 10px;
}

.box {
  width: 100px;
  height: 100px;
  border-radius: 10px;
  background-color: yellow;
}
</style>
