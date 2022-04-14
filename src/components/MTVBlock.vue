<template>
  <BlockBuilder
    title="MTV"
    icon="mtv.svg"
    :counter="mtvCounter"
    @changeCount="changeCount"
  />
</template>

<script>
import BlockBuilder from "./BlockBuilder.vue";
export default {
  name: "ServerBlock",
  props: ["mtvCounter"],
  components: {
    BlockBuilder,
  },
  methods: {
    changeCount(data) {
      this.$emit("updateMTV", {
        name: "mtvCounter",
        value: +data,
      });
    },
  },
};
</script>

<style></style>
