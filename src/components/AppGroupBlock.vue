<template>
  <BlockBuilder
    title="App group"
    icon="app-group_icon.svg"
    :counter="appGroupCounter"
    @changeCount="changeCount"
  />
</template>

<script>
import BlockBuilder from "./BlockBuilder.vue";
export default {
  name: "appGroupBlock",
  props: ["appGroupCounter"],
  components: {
    BlockBuilder,
  },
  methods: {
    changeCount(data) {
      this.$emit("updateAppGroup", {
        name: "appGroupCounter",
        value: +data,
      });
    },
  },
};
</script>
