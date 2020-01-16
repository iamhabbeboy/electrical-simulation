<template>
  <div>
    <h4>Selection</h4>
    <!-- <div v-if="listDevice"> -->
      <div v-for="(device, index) of listDevice" :key="index">
        {{ index }}: {{ device }}
      </div>
    <!-- </div> -->
		{{ listDevice }}
  </div>
</template>
<script>
import { EventBus } from "@/event-bus.js";

export default {
  data() {
    return {
      device: []
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
      this.device.push(value);
    });
  }
};
</script>
