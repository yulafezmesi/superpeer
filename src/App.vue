<template>
  <div class="container">
    <div class="card">
      <small class="call-title">Call with</small>
      <h3 class="call-name">Niloya Kayıkçı</h3>
      <div class="call-date-info">
        <span class="call-date-time">
          <app-calendar iconColor="var(--primary-color)"></app-calendar>
          <small>7 Oct, Weds</small>
        </span>
        <span class="call-date-time">
          <app-clock iconColor="var(--primary-color)"></app-clock>
          <small>10:15AM - 10:30AM</small>
        </span>
      </div>
      <small class="call-time-zone">Timezone: Europe/Amsterdam</small>
      <figure class="call-thumb">
        <img src="./assets/images/bgc.jpg" />
        <div class="call-iconset">
          <app-microphone tabindex="1" circle></app-microphone>
          <app-camera tabindex="2" circle></app-camera>
          <app-settings tabindex="3" circle></app-settings>
        </div>
      </figure>
      <app-input type="text" v-model="code">
        <app-user iconColor="var(--primary-color)"></app-user>
      </app-input>
      <div class="hardware-wrapper">
        <app-dropdown label="Camera">
          <option>Facetime HD Camera</option>
        </app-dropdown>
        <app-dropdown label="Speaker">
          <option>Built-in Output (Headp...</option>
        </app-dropdown>
        <app-dropdown label="Microphone">
          <option>Built-in Microphone (E...</option>
        </app-dropdown>
        <div class="call-sound">
          <span>Sound Test</span>
          <app-button type="outline">Play Sound</app-button>
        </div>
      </div>
      <div class="join-call">
        <app-button type="primary" isFull>Join Call</app-button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data: function () {
    return {
      code: "",
    };
  },
  components: {
    AppCalendar: () => import("./components/Icons/Calendar"),
    AppMicrophone: () => import("./components/Icons/Microphone"),
    AppCamera: () => import("./components/Icons/Camera"),
    AppSettings: () => import("./components/Icons/Options"),
    AppClock: () => import("./components/Icons/Clock"),
    AppUser: () => import("./components/Icons/User"),
    AppInput: () => import("./components/Inputs/Input"),
    AppDropdown: () => import("./components/Inputs/Dropdown"),
    AppButton: () => import("./components/Buttons/Button"),
  },
};
</script>

<style>
.container {
  display: flex;
  align-items: center;
  justify-content: center;
}
.card {
  background-color: #fff;
  box-shadow: 0 0.5em 1em -0.125em rgba(10, 10, 10, 0.1),
    0 0 0 1px rgba(10, 10, 10, 0.02);
  border-radius: var(--default-radius);
  max-width: 100%;
  position: relative;
  overflow: hidden;
  padding: var(--default-padding);
  margin: 1rem;
}
.call-title {
  text-align: center;
  color: var(--primary-color);
  display: inline-block;
  text-align: center;
  width: 100%;
}
.call-name {
  font-weight: bold;
  margin-top: 0.1rem;
  margin-bottom: 0.7rem;
  text-align: center;
  color: var(--gray-90);
}
.call-date-info {
  display: flex;
  padding: var(--default-padding);
  border: 1px solid var(--border-gray);
  border-radius: var(--default-radius);
  justify-content: space-between;
}
.call-date-time {
  display: inline-flex;
  align-items: center;
}
.call-date-time small {
  margin-left: 0.5rem;
}
.call-time-zone {
  color: var(--gray-80);
  width: 100%;
  text-align: center;
  display: inline-block;
}
.call-thumb {
  position: relative;
}
.call-thumb img {
  max-width: 300px;
  border-radius: var(--default-radius);
}
.call-iconset {
  display: flex;
  gap: 1rem;
  justify-content: center;
  position: absolute;
  width: 100%;
  bottom: 1.2rem;
}
.call-sound {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.call-sound span {
  font-size: 14px;
}
.hardware-wrapper {
  display: grid;
  gap: 0.5rem;
}
.join-call {
  margin-top: 1rem;
}
</style>
