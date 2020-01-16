<template>
  <div>
    <h1>Simulation</h1>
    <div class="simulator">
      <div class="inner-simulator">
        <div style="padding-bottom: 10px;padding-top: 10px;">
          <h3 style="text-align:center">Simulator Box</h3>
        </div>
        <div class="simulator-box">
          <div v-for="(appliance, index) of appliances" :key="index">
            <Element :url="appliance.image" />
          </div>
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
  min-height: 420px;
  background: #ffffff;
  border: 5px solid gold;
  .inner-simulator {
    min-height: 200px;
    border-bottom: 3px solid orange;
  }
}

.simulator-box {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
}

.pole-holder {
  padding-right: 20px;
  padding-left: 20px;
  padding-bottom: 45px;
  border-bottom: 3px solid orange;
  height: 40px;
  margin-bottom: 25px;

  :nth-child(2) {
    height: inherit;
    position: relative;
    bottom: 7px;
  }
}
.pole-wire {
  background: orange !important;
  height: 100%;
  width: 10%;
  margin: auto;
}
</style>
