<template>
  <BlockBuilder
    title="Functions"
    icon="functions_icon.svg"
    :counter="functionsCounter"
    @changeCount="changeCount"
  />
</template>

<script>
import BlockBuilder from "./BlockBuilder.vue";
export default {
  name: "FunctionsBlock",
  props: ["functionsCounter"],
  components: {
    BlockBuilder,
  },
  methods: {
    changeCount(data) {
      this.$emit("updateFunctions", {
        name: "functionsCounter",
        value: +data,
      });
    },
  },
};
</script>

<style></style>
