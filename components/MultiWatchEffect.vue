<script setup lang="ts">
const count = ref(0);
const count2 = ref(0);
watchEffect(() => {
  console.log('MultiWatchEffect', 'count', count.value, 'count2', count2.value);
});
const onClick = () => {
  count.value++;
};
const onClick2 = () => {
  count2.value++;
};
const onClick3 = () => {
  count.value = count.value;
};
</script>

<template>
  <div>
    <h2>MultiWatchEffect</h2>
    <p>Count: {{ count }}</p>
    <p>Count2: {{ count2 }}</p>
    <button @click="onClick">count1 Increment</button>
    <button @click="onClick2">count2 Increment</button>
    <button @click="onClick3">count1 Same</button>
  </div>
</template>
