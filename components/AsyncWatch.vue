<script setup lang="ts">
const count = ref(0);
watch(count, async () => {
  await new Promise((resolve) => setTimeout(resolve, 1000));
  console.log('AsyncWatch', 'count', count.value);
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
    <h2>AsyncWatch</h2>
    <p>Count: {{ count }}</p>
    <button @click="onClick">Increment</button>
    <button @click="onClick2">Same</button>
    <button @click="onClick3">Increment and Decrement</button>
  </div>
</template>
