<template>
  <div class="builder">
    <img
      :src="require(`../assets/images/${icon}`)"
      :alt="title"
      class="builder__icon"
    />
    <h2 class="builder__title">{{ title }}</h2>
    <div class="builder__counter">
      <input
        class="builder__counter__input"
        type="number"
        v-model="count"
        @change="changeCount"
      />
    </div>
  </div>
</template>
<script>
export default {
  name: "BlockBuilder",
  data() {
    return {
      count: this.counter,
    };
  },
  components: {},
  props: ["icon", "title", "counter"],
  methods: {
    changeCount() {
      this.$emit("changeCount", this.count);
    },
  },
};
</script>

<style lang="less">
@import "../assets/layouts/index.less";
</style>
