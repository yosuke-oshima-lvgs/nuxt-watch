<script setup lang="ts">
const count = ref(0);
watch(
  count,
  () => {
    console.log('WatchImmediate', 'count', count.value);
  },
  {
    immediate: true,
  }
);
const onClick = () => {
  count.value++;
};
const onClick2 = () => {
  count.value = count.value;
};
const onClick3 = () => {
  count.value++;
  count.value--;
};
</script>

<template>
  <div>
    <h2>WatchImmediate</h2>
    <p>Count: {{ count }}</p>
    <button @click="onClick">Increment</button>
    <button @click="onClick2">Same</button>
    <button @click="onClick3">Increment and Decrement</button>
  </div>
</template>
