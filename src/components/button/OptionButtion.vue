<script setup lang="ts">
defineProps<{
  disabled?: boolean
}>()
</script>

<template>
  <button class="btn-option" :disabled="disabled">
    <span class="btn-text">
      <slot>Text</slot>
    </span>
  </button>
</template>

<style scoped>
/* ===== Button / Option (Default) ===== */
.btn-option {
  box-sizing: border-box;

  /* Auto layout */
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 32px;

  width: 318px;
  max-width: 318px;
  height: 72px;
  min-height: 72px;

  padding: 12px 28px;

  background: #ffffff;
  border-radius: 32px;
  border: none;

  cursor: pointer;
  user-select: none;
}

/* ===== Text ===== */
.btn-text {
  max-width: 262px;
  height: 24px;

  font-family: 'Poppins', system-ui, sans-serif;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;

  color: #766630;
}

/* ===== Active（Property 1 = Active） ===== */
.btn-option:active {
  background: #e9debb;
}

/* ===== Disabled（Property 1 = Disabled） ===== */
.btn-option:disabled {
  background: rgba(233, 222, 187, 0.45);
  cursor: not-allowed;
}

.btn-option:disabled .btn-text {
  color: rgba(118, 102, 48, 0.45);
}
</style>
