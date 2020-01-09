<template>
  <div>
    <h4>
      <span style="cursor:pointer">Size</span> /
      <span style="cursor:pointer">Expert Mode</span>
    </h4>
    <a
      href="javascript:void(0)"
      @click="selection"
      v-for="(size, index) of sizes.data"
      :key="index"
      :data-size="size"
      >{{ index }}</a
    >
  </div>
</template>

<script>
import { EventBus } from "@/event-bus.js";

export default {
  data() {
    return {
      id: "",
      image: "",
      sizes: {}
    };
  },
  mounted() {
    EventBus.$on("WATT", value => {
      this.sizes = value;
    });
  },
  methods: {
    selection(e) {
      const el = e.currentTarget;
      const size = el.getAttribute("data-size");
      EventBus.$emit("ADD", {
        id: this.sizes.id,
        size: size,
        image: this.sizes.image
      });
      this.sizes = {};
    }
  }
};
</script>
