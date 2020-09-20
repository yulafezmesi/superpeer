<template>
  <div class="wrapper">
    <label v-if="label">{{label}}</label>
    <div class="dropdown-wrapper">
      <select ref="select" @input="updateModel($event.target.value)">
        <slot />
      </select>
      <span class="dropdown-wrapper-icon">
        <app-dropdown-icon></app-dropdown-icon>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Button",
  props: {
    label: {
      type: String,
    },
    model: {},
  },
  methods: {
    updateModel(val) {
      this.$emit("input", val);
    },
  },
  components: {
    AppDropdownIcon: () => import("../Icons/Dropdown"),
  },
};
</script>

<style scoped>
.wrapper {
  display: flex;
  justify-content: space-between;
  align-self: center;
  font-size: var(--body-font);
}
.wrapper label {
  text-align: center;
  display: block;
  line-height: 2.2;
  height: 100%;
  margin-right: 1.5rem;
}
.dropdown-wrapper {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid var(--border-gray);
  border-radius: var(--default-radius);
  min-width: 200px;
}
.dropdown-wrapper-icon {
  position: absolute;
  right: 5%;
  pointer-events: none;
}
select {
  padding: var(--default-padding);
  border: none;
  border-radius: var(--default-radius);
  width: 100%;
  appearance: none;
}
</style>
