<template>
  <TabViewComponent :currentTabIndex="currentTabIndex" />
  <BottomBarComponent @changeTab="changeTab" />
</template>

<script>
import TabViewComponent from "@/components/TabView.vue";
import BottomBarComponent from "@/components/BottomBar.vue";
import { ref } from "vue";
export default {
  components: { BottomBarComponent, TabViewComponent },
  setup() {
    const currentTabIndex = ref(0);

    const changeTab = (index) => {
      currentTabIndex.value = index;
    };
    return {
      BottomBarComponent,
      TabViewComponent,
      changeTab,
      currentTabIndex,
    };
  },
};
</script>

<style>
</style>