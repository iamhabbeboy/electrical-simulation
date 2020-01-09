<template>
  <div>
    <h1>Simulation</h1>
    <div class="simulator">
      <div style="height: 200px;border-bottom: 3px solid orange;">
        <div style="padding-bottom: 10px;padding-top: 10px;">
          <h3>Simulator Box</h3>
        </div>
        <div v-for="(appliance, index) of appliances" :key="index">
          <Element :url="appliance.image" />
        </div>
      </div>
      <div style="clear:both;width: 20%;margin: 0px auto;text-align:center;">
        <div style="width: 5px;height: 100px;background: orange;float:left">
          &nbsp;
        </div>
        <div style="width: 5px;height: 100px;background: orange;float:right">
          &nbsp;
        </div>
        <div style="clear:both;border-top: 3px solid orange;">
          <img
            src="../assets/inverter.svg"
            width="100"
            style="position: relative;bottom: 20px;"
          />
        </div>
      </div>
    </div>
    <!-- {{ appliances }} -->
  </div>
</template>

<script>
import { EventBus } from "@/event-bus.js";
import Element from "@/components/Element.vue";
export default {
  components: {
    Element
  },
  data() {
    return {
      appliances: []
    };
  },
  mounted() {
    EventBus.$on("ADD", value => {
      this.appliances.push(value);
    });
  }
};
</script>
<style lang="scss">
.simulator {
  height: 420px;
  background: #ffffff;
  border: 5px solid gold;
  div.pole-holder {
    float: left;
    margin-right: 20px;
    margin-left: 20px;
    height: 60px;
    :nth-child(2) {
      height: inherit;
    }
  }
}
.pole-wire {
  background: orange !important;
  height: 100%;
  width: 10%;
  margin: auto;
}
</style>
