<template>
  <div class="circle" v-if="circle">
    <svg
      :width="width"
      :height="height"
      :viewBox="viewBox"
      :fill="iconColor"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        fill-rule="evenodd"
        clip-rule="evenodd"
        d="M12 9.75H9C8.586 9.75 8.25 9.41475 8.25 9V6C8.25 5.58525 8.586 5.25 9 5.25C9.414 5.25 9.75 5.58525 9.75 6V8.25H12C12.4148 8.25 12.75 8.58525 12.75 9C12.75 9.41475 12.4148 9.75 12 9.75ZM9 1.5C4.8645 1.5 1.5 4.8645 1.5 9C1.5 13.1355 4.8645 16.5 9 16.5C13.1355 16.5 16.5 13.1355 16.5 9C16.5 4.8645 13.1355 1.5 9 1.5Z"
      />
      <mask
        id="mask0"
        mask-type="alpha"
        maskUnits="userSpaceOnUse"
        x="1"
        y="1"
        width="16"
        height="16"
      >
        <path
          fill-rule="evenodd"
          clip-rule="evenodd"
          d="M12 9.75H9C8.586 9.75 8.25 9.41475 8.25 9V6C8.25 5.58525 8.586 5.25 9 5.25C9.414 5.25 9.75 5.58525 9.75 6V8.25H12C12.4148 8.25 12.75 8.58525 12.75 9C12.75 9.41475 12.4148 9.75 12 9.75ZM9 1.5C4.8645 1.5 1.5 4.8645 1.5 9C1.5 13.1355 4.8645 16.5 9 16.5C13.1355 16.5 16.5 13.1355 16.5 9C16.5 4.8645 13.1355 1.5 9 1.5Z"
          fill="white"
        />
      </mask>
      <g mask="url(#mask0)" />
    </svg>
  </div>
  <svg
    v-else
    :width="width"
    :height="height"
    :viewBox="viewBox"
    :fill="iconColor"
    xmlns="http://www.w3.org/2000/svg"
  >
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M12 9.75H9C8.586 9.75 8.25 9.41475 8.25 9V6C8.25 5.58525 8.586 5.25 9 5.25C9.414 5.25 9.75 5.58525 9.75 6V8.25H12C12.4148 8.25 12.75 8.58525 12.75 9C12.75 9.41475 12.4148 9.75 12 9.75ZM9 1.5C4.8645 1.5 1.5 4.8645 1.5 9C1.5 13.1355 4.8645 16.5 9 16.5C13.1355 16.5 16.5 13.1355 16.5 9C16.5 4.8645 13.1355 1.5 9 1.5Z"
    />
    <mask
      id="mask0"
      mask-type="alpha"
      maskUnits="userSpaceOnUse"
      x="1"
      y="1"
      width="16"
      height="16"
    >
      <path
        fill-rule="evenodd"
        clip-rule="evenodd"
        d="M12 9.75H9C8.586 9.75 8.25 9.41475 8.25 9V6C8.25 5.58525 8.586 5.25 9 5.25C9.414 5.25 9.75 5.58525 9.75 6V8.25H12C12.4148 8.25 12.75 8.58525 12.75 9C12.75 9.41475 12.4148 9.75 12 9.75ZM9 1.5C4.8645 1.5 1.5 4.8645 1.5 9C1.5 13.1355 4.8645 16.5 9 16.5C13.1355 16.5 16.5 13.1355 16.5 9C16.5 4.8645 13.1355 1.5 9 1.5Z"
        fill="white"
      />
    </mask>
    <g mask="url(#mask0)" />
  </svg>
</template>
<script>
export default {
  props: {
    viewBox: { type: String, default: "0 0 18 18" },
    width: { type: [Number, String], default: 18 },
    height: { type: [Number, String], default: 18 },
    iconColor: { type: String, default: "#222222" },
    circle: { type: Boolean, default: false },
  },
};
</script>

<style scoped>
.circle {
  width: 48px;
  height: 48px;
  display: flex;
  background-color: var(--default-gray);
  justify-content: center;
  align-items: center;
  border-radius: 50%;
}
</style>