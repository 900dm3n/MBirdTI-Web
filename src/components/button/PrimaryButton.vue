<script setup lang="ts">
defineProps<{
  disabled?: boolean
}>()
</script>

<template>
  <button class="btn-primary" :disabled="disabled">
    <span class="btn-text">
      <slot>Text</slot>
    </span>

    <span class="btn-icon" aria-hidden="true"> → </span>
  </button>
</template>

<style scoped>
/* ===== Button / Primary (Default) ===== */
.btn-primary {
  position: relative;

  width: 180px;
  min-width: 180px;
  height: 48px;

  background: #564a24;
  border-radius: 32px;
  border: none;

  display: inline-flex;
  align-items: center;
  cursor: pointer;
  user-select: none;
}

/* ===== Text ===== */
.btn-text {
  position: absolute;
  left: 24px;
  top: 14px;

  width: 108px;
  min-width: 108px;
  height: 20px;

  display: flex;
  align-items: center;
  justify-content: center;

  font-family: 'Poppins', system-ui, sans-serif;
  font-weight: 500;
  font-size: 16px;
  line-height: 20px;

  color: #ffffff;
}

/* ===== Icon / arrow-right ===== */
.btn-icon {
  position: absolute;
  left: 140px;
  top: 12px;

  width: 24px;
  height: 24px;

  display: flex;
  align-items: center;
  justify-content: center;

  font-size: 20px;
  line-height: 1;
  color: #ffffff;
}

/* ===== Active（Property 1 = Active） ===== */
.btn-primary:active {
  background: rgba(86, 74, 36, 0.85);
}

/* ===== Disabled（Property 1 = Disabled） ===== */
.btn-primary:disabled {
  background: rgba(86, 74, 36, 0.45);
  cursor: not-allowed;
}
</style>
