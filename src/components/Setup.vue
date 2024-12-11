<script setup lang="ts">
export interface Props {
  msg: string;
}

defineProps<Props>();
</script>

<template>
  <div>{{ msg }}</div>
</template>
