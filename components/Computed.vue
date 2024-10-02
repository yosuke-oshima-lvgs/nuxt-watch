<script setup lang="ts">
const count = ref(0);
const computedCount = computed(() => {
  console.log('Computed', 'count', count.value);
  return count.value;
});

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
    <h2>Computed</h2>
    <p>Count: {{ count }}</p>
    <p>computedCount: {{ computedCount }}</p>
    <button @click="onClick">Increment</button>
    <button @click="onClick2">Same</button>
    <button @click="onClick3">Increment and Decrement</button>
  </div>
</template>
