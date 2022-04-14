<template>
  <BlockBuilder
    title="Interface"
    icon="interface_icon.svg"
    :counter="interfaceCounter"
    @changeCount="changeCount"
  />
</template>

<script>
import BlockBuilder from "./BlockBuilder.vue";
export default {
  name: "InterfaceBlock",
  props: ["interfaceCounter"],
  components: {
    BlockBuilder,
  },
  methods: {
    changeCount(data) {
      this.$emit("updateInterface", {
        name: "interfaceCounter",
        value: +data,
      });
    },
  },
};
</script>

<style></style>
