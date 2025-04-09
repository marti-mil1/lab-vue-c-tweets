<script setup>
const props = defineProps({
    user: {
        name: {
            type: String,
            default: "Thoughts of Dog®",
        },
        handle: {
            type: String,
            default: "dog_feelings"
        },
    },
})
</script>

<template>
    <span class="name">{{ user.name }}</span>
    <span class="handle">{{ user.handle }}</span>
</template>

<style scoped>
.name {
    font-weight: bold;
    margin-bottom: 0.5em;
    margin-right: 0.3em;
  }

  .handle {
    color: #536471;
    margin-left: 3px;
    margin-right: 3px;
  }
</style>
