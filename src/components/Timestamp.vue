<script setup>
const props = defineProps({
    timestamp: {
        type: String,
        required: true
    }
})
</script>

<template>
   <span class="timestamp">{{ timestamp }}</span>
</template>

<style scoped>
 .timestamp {
    color: #536471;
    font-size: 1.1rem;
  }

  .timestamp::before {
    content: "·";
    padding-right: 0.3em;
    font-size: 1.1rem;
    font-weight: 600;
  }
</style>
