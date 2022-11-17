<script setup>
const props = defineProps(['name', 'stats', 'alignment'])
</script>

<template>
  <div :class="alignment">
    <h1>{{ name }}</h1>
    <StatField v-for="(value, key) in stats" :key="key" :skill="key" :value="value">
      {{ key }} : {{ value }}
    </StatField>
  </div>
</template>

<style scoped>
.bad
{
    background-image: linear-gradient(to right, #f12711, #f5af19);
}
.good
{
    background-image: linear-gradient(135deg, #81b000, #00e439);
}
.neutral
{
    background-image: linear-gradient(135deg, #e200bc, #8a3dc9);
}
</style>