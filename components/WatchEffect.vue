<script setup lang="ts">
const count = ref(0);
watchEffect(() => {
  console.log('WatchEffect', 'count', count.value);
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
    <h2>WatchEffect</h2>
    <p>Count: {{ count }}</p>
    <button @click="onClick">Increment</button>
    <button @click="onClick2">Same</button>
  </div>
</template>
