<template>
  <div class="tab-view">
    <template v-for="(content, index) in data" :key="index">
      <TabComponent :content="content" v-if="currentTabIndex == index" />
    </template>
  </div>
</template>

<script>
import TabComponent from "@/components/Tab.vue";
export default {
  components: { TabComponent },
  props: {
    currentTabIndex: {
      type: Number,
      default: 0,
    },
  },
  setup() {
    const data = [
      {
        title: "First Tab",
        text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente similique mollitia iusto consectetur pariatur voluptatem maxime vero. Suscipit atque quam enim, quo inventore pariatur earum ipsam sunt rem odit voluptatem?",
      },
      {
        title: "Second Tab",
        text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. ",
      },
      {
        title: "Third Tab",
        text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente similique mollitia iusto consectetur pariatur voluptatem maxime vero.",
      },
    ];

    return {
      data,
    };
  },
};
</script>

<style lang="scss" scoped>
.tab-view {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 50px;

  &__tab {
    margin-top: 30px;
  }
}
</style>