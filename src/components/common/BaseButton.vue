<script setup>
defineProps({
  variant: {
    type: String,
    default: 'primary',
  },
  type: {
    type: String,
    default: 'button',
  },
  href: {
    type: String,
    default: '',
  },
})
</script>

<template>
  <a
    v-if="href"
    :href="href"
    target="_blank"
    rel="noopener noreferrer"
    :class="['base-button', `base-button--${variant}`]"
  >
    <slot />
  </a>

  <button v-else :type="type" :class="['base-button', `base-button--${variant}`]">
    <slot />
  </button>
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
  border: none;
}

.base-button:hover {
  transform: translateY(-3px);
}
.base-button--primary {
  background: var(--primary);
  color: white;
}

.base-button--success {
  background: #25d366;
  color: white;
}
</style>
