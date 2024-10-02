<script setup lang="ts">
const count = ref(0);
const computedCount = computed(async () => {
  await new Promise((resolve) => setTimeout(resolve, 1000));
  console.log('AsyncComputed', 'count', count.value);
  return count.value;
});

const onClick = () => {
  count.value++;
};
const onClick2 = () => {
  count.value = count.value;
};
</script>

<template>
  <div>
    <h2>AsyncComputed</h2>
    <p>Count: {{ count }}</p>
    <p>computedCount: {{ computedCount }}</p>
    <button @click="onClick">Increment</button>
    <button @click="onClick2">Same</button>
  </div>
</template>
