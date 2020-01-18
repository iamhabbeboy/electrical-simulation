<template>
  <div>
    <h4>Selection</h4>
    <div v-for="(device, index) of listDevice" :key="index">
      {{ index | toUFirst }}: {{ device }}
    </div>
    <div v-if="!listDevice">
      <p>No appliances selected</p>
    </div>
  </div>
</template>
<script>
import { EventBus } from "@/event-bus.js";

export default {
  data() {
    return {
      device: [],
      MAX_WATT: 7000
    };
  },
  computed: {
    listDevice() {
      if (this.device.length === 0) {
        return;
      }
      let counter = {};
      this.device.map(device => {
        counter[device.image] = ++counter[device.image] || 1;
      });
      return counter;
    }
  },
  mounted() {
    EventBus.$on("ADD", value => {
      // if (this.totalWatt <= this.MAX_WATT) {
      this.device.push(value);
      // }
    });
  },
  filters: {
    toUFirst(value) {
      return value.substring(0, 1).toUpperCase() + "" + value.substring(1);
    }
  }
};
</script>
