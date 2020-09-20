<template>
  <button :class="[
     `button is-${type} `,
      isFull ? 'is-full' : null,
    ]">
    <slot />
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    type: {
      default: "primary",
    },
    isFull: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style scoped>
.button {
  padding: var(--default-padding);
  border-radius: var(--default-radius);
  background-color: transparent;
  min-width: 200px;
  font-size: var(--body-font);
}
.is-outline {
  color: var(--primary-color);
  border: 1px solid var(--primary-color);
}
.is-primary {
  border: none;
  color: white;
  background-color: var(--primary-color);
}
.is-full {
  width: 100% !important;
}
</style>
