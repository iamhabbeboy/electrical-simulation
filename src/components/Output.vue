<template>
  <div>
    <h4>Output</h4>
    <div style="text-align: center">
      <h1>1.5KVA</h1>
      <p>Total Watt: {{ totalWatt }}W</p>
    </div>
  </div>
</template>
<script>
import { EventBus } from "@/event-bus.js";

export default {
  data() {
    return {
      watts: []
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
			return total; //eslint-disable-line
    }
  },
  mounted() {
    EventBus.$on("ADD", value => {
      this.watts.push(value);
    });
  }
};
</script>
