<template>
  <BlockBuilder
    title="Server"
    icon="server.svg"
    :counter="serverCounter"
    @changeCount="changeCount"
  />
</template>

<script>
import BlockBuilder from "./BlockBuilder.vue";
export default {
  name: "ServerBlock",
  props: ["serverCounter"],
  components: {
    BlockBuilder,
  },
  methods: {
    changeCount(data) {
      this.$emit("updateServer", {
        name: "serverCounter",
        value: +data,
      });
    },
  },
};
</script>

<style lang="less"></style>
