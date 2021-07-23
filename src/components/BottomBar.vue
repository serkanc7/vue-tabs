<template>
  <footer class="bottom-bar">
    <template v-for="(icon, index) in icons" :key="index">
      <span @click="$emit('changeTab', index)" class="bottom-bar__icon">
        <img :src="icon" alt="" />
      </span>
    </template>
  </footer>
</template>

<script>
export default {
  emits: ["changeTab"],
  setup() {
    const icons = [
      "/src/assets/svg/home.svg",
      "/src/assets/svg/whatshot.svg",
      "/src/assets/svg/album.svg",
    ];
    return {
      icons,
    };
  },
};
</script>

<style lang="scss" scoped>
.bottom-bar {
  height: 75px;
  background: #b05b3b;
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-evenly;

  &__icon {
    cursor: pointer;
  }
}
</style>