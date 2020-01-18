<template>
  <div>
    <h4>Inverter Recommendation</h4>
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
      powerFactor: 0.8,
      CONVERT_TO_KV: 1000,
      MAX_WATT: 7000,
      TOLERANCE: 0.3,
      inverters: [1.2, 2.5, 3.0, 3.5, 4.0, 5.0, 7.5, 10]
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
      let output = 0;
      let result = this.totalWatt / this.powerFactor;
      result = result / this.CONVERT_TO_KV;
      result = result + this.TOLERANCE;
      if (result <= 0) {
        return 0;
      }
      result = result.toFixed(2);
      const recommendation = this.inverterRecommendation(result);
      this.storage(recommendation);
      return recommendation;
    },
    appliances() {
      return this.watts.length;
    }
  },
  methods: {
    inverterRecommendation(target) {
      const closest = this.inverters.reduce((prev, curr) => {
        return Math.abs(curr - target) < Math.abs(prev - target) ? curr : prev;
      });
      return closest;
    },
    storage(data) {
      const date = new Date();
      const store = {
        time: date,
        data: data,
        watt: this.totalWatt
      };
      localStorage.setItem("_SIMULATION_DATA", JSON.stringify(store));
    }
  },
  mounted() {
    EventBus.$on("ADD", value => {
      if (this.totalWatt <= this.MAX_WATT) {
        this.watts.push(value);
      }
    });
  }
};
</script>
