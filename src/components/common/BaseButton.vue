<script setup>
defineProps({
  variant: {
    type: String,
    default: 'primary',
  },
})
</script>

<template>
  <button :class="`btn btn-${variant} base-button`"><slot /></button>
</template>

<style scoped>
.base-button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  border-radius: 50px;
  padding: 12px 30px;
  font-weight: 600;
  transition: all 0.3s ease;
}

.base-button:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
}
</style>
