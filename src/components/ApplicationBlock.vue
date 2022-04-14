<template>
  <div class="application">
    <div class="application-info">
      <img
        class="application-info__icon"
        src="../assets/images/application.svg"
        alt="Application"
      />
      <h2 class="application-info__title">Application</h2>
      <div class="application-info__counter">
        <input
          type="text"
          :value="applicationCount()"
          class="builder__counter__input"
          disabled
        />
      </div>
    </div>

    <div class="block__app-group">
      <div class="block__app-group__group">
        <AppGroupBlock
          @updateAppGroup="change"
          :appGroupCounter="counters.appGroupCounter"
        />
        <div class="line-to-application__app-group">
          <img src="../assets/images/line-1.svg" />
        </div>
      </div>
    </div>

    <div class="block__server">
      <div class="block__server__group">
        <ServerBlock
          @updateServer="change"
          :serverCounter="counters.serverCounter"
        />
        <div class="line-to-application__server">
          <img src="../assets/images/line-1.svg" />
        </div>
      </div>
    </div>

    <div class="block__mtv">
      <div class="block__mtv__group">
        <MTVBlock @updateMTV="change" :mtvCounter="counters.mtvCounter" />
        <div class="line-to-application__mtv">
          <img src="../assets/images/line-1.svg" />
        </div>
      </div>
    </div>

    <div class="block__functions">
      <div class="block__functions__group">
        <FunctionsBlock
          @updateFunctions="change"
          :functionsCounter="counters.functionsCounter"
        />
        <div class="line-to-application__functions">
          <img src="../assets/images/line-2.svg" />
        </div>
      </div>
    </div>

    <div class="block__interface">
      <div class="block__interface__group">
        <InterfaceBlock
          @updateInterface="change"
          :interfaceCounter="counters.interfaceCounter"
        />
        <div class="line-to-application__interface__1">
          <img src="../assets/images/line-2.svg" />
        </div>
        <div class="line-to-application__interface__2">
          <img src="../assets/images/line-2.svg" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AppGroupBlock from "./AppGroupBlock.vue";
import ServerBlock from "./ServerBlock.vue";
import MTVBlock from "./MTVBlock.vue";
import FunctionsBlock from "./FunctionsBlock.vue";
import InterfaceBlock from "./InterfaceBlock.vue";

export default {
  name: "ApplicationBlock",
  data() {
    return {
      counters: {
        appGroupCounter: 66,
        functionsCounter: 133,
        interfaceCounter: 223,
        mtvCounter: 224,
        serverCounter: 55,
      },
    };
  },
  components: {
    AppGroupBlock,
    ServerBlock,
    MTVBlock,
    FunctionsBlock,
    InterfaceBlock,
  },
  methods: {
    change(data) {
      this.counters[data.name] = data.value;
    },
    applicationCount() {
      let sum = 0;
      Object.values(this.counters).forEach((val) => (sum += val));
      return sum;
    },
  },
};
</script>

<style lang="less">
@import "../assets/layouts/index.less";
</style>
