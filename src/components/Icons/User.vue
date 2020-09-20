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
        d="M19 20C19 20.552 18.553 21 18 21C17.447 21 17 20.552 17 20C17 17.243 14.757 15 12 15C9.243 15 7 17.243 7 20C7 20.552 6.553 21 6 21C5.447 21 5 20.552 5 20C5 16.14 8.141 13 12 13C15.859 13 19 16.14 19 20ZM12 5C13.103 5 14 5.897 14 7C14 8.103 13.103 9 12 9C10.897 9 10 8.103 10 7C10 5.897 10.897 5 12 5ZM12 11C14.206 11 16 9.206 16 7C16 4.794 14.206 3 12 3C9.794 3 8 4.794 8 7C8 9.206 9.794 11 12 11Z"
      />
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
      d="M19 20C19 20.552 18.553 21 18 21C17.447 21 17 20.552 17 20C17 17.243 14.757 15 12 15C9.243 15 7 17.243 7 20C7 20.552 6.553 21 6 21C5.447 21 5 20.552 5 20C5 16.14 8.141 13 12 13C15.859 13 19 16.14 19 20ZM12 5C13.103 5 14 5.897 14 7C14 8.103 13.103 9 12 9C10.897 9 10 8.103 10 7C10 5.897 10.897 5 12 5ZM12 11C14.206 11 16 9.206 16 7C16 4.794 14.206 3 12 3C9.794 3 8 4.794 8 7C8 9.206 9.794 11 12 11Z"
    />
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


