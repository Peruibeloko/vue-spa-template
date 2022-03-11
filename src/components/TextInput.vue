<template>
  <div class="input-wrapper">
    <label>
      {{ props.label }}
    </label>
    <input
      class="input"
      type="text"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
    />
  </div>
</template>

<script setup>
const props = defineProps(['label', 'modelValue']);
defineEmits(['update:modelValue']);
</script>

<style scoped></style>
