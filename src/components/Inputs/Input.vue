<template>
  <div class="input-wrapper">
    <slot />
    <input :type="type" :value="model" @input="updateModel($event.target.value)" />
  </div>
</template>

<script>
export default {
  name: "Button",
  props: {
    type: {
      required: true,
      default: "text",
    },
    model: {
      default: "Adem İlter",
    },
  },
  methods: {
    updateModel(val) {
      this.$emit("input", val);
    },
  },
};
</script>

<style scoped>
.input-wrapper {
  display: inline-flex;
  align-items: center;
  padding: var(--default-padding);
  border: 1px solid var(--border-gray);
  border-radius: var(--default-radius);
  width: 100%;
  margin-bottom: 0.5rem;
}

input {
  border: none;
  height: 100%;
  padding-left: 8px;
  font-size: var(--body-font);
}
input:focus {
  outline: none;
}
</style>
