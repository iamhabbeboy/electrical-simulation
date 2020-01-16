<template>
  <div>
    <h4>Output</h4>
    <div style="text-align: center">
      <h1>{{ power }} KVA</h1>
      <p>Total Watt: {{ totalWatt }}W</p>
      <p style="font-size: 12px;font-weight:bold;">
        Total Appliances Connected: {{ appliances }}
      </p>
    </div>
  </div>
</template>
<script>
import { EventBus } from "@/event-bus.js";

export default {
  data() {
    return {
      watts: [],
      powerFactor: 0.8
    };
  },
  computed: {
    totalWatt() {
      let total = 0;
      if (this.watts.length == 0) {
        return total;
      }
      this.watts.map(el => {
        total += parseInt(el.size);
      });
      return total;
    },
    power() {
      if (this.totalWatt === 0) {
        return 0;
      }
      const result = this.totalWatt / this.powerFactor;
      if (result <= 0) {
        return 0;
      }
      return Math.floor(result);
    },
    appliances() {
      return this.watts.length;
    }
  },
  mounted() {
    EventBus.$on("ADD", value => {
      this.watts.push(value);
    });
  }
};
</script>
