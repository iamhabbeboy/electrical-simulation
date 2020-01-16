<template>
  <div class="appliance">
    <div class="app-holder">
      <div class="list-holder">
        <h4>Select Appliances</h4>
        <a
          href="javascript:void(0)"
          @click="selected"
          v-for="(appliance, index) of appliances"
          :key="index"
          :data-id="appliance.id"
          :data-img="appliance.image"
          :data-size="`${JSON.stringify(appliance.size)}`"
        >
          {{ appliance.name }}
        </a>
      </div>
      <div class="list-holder">
        <Category />
      </div>
      <div>
        <Selection />
      </div>
      <div>
        <h4>Recommendation</h4>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam odit
          quaerat deleniti quia voluptatibus earum aliquam, ut fugit culpa unde
          minus reprehenderit totam repellendus nihil alias perspiciatisratione
          voluptatem et.
        </p>
      </div>
      <div>
        <Output />
      </div>
    </div>
  </div>
</template>
<script>
import json from "../assets/data/appliances.json";
import Category from "@/components/Category.vue";
import Selection from "@/components/Selection.vue";
import Output from "@/components/Output.vue";
import { EventBus } from "@/event-bus.js";

export default {
  components: {
    Category,
    Output,
    Selection
  },
  data() {
    return {
      appliances: json,
      sizes: {}
    };
  },
  methods: {
    selected(e) {
      const el = e.currentTarget;
      const appId = el.getAttribute("data-id");
      const size = el.getAttribute("data-size");
      const img = el.getAttribute("data-img");
      if (size.length < 5) {
        EventBus.$emit("ADD", { id: appId, size: size, image: img });
      } else {
        EventBus.$emit("WATT", {
          id: appId,
          image: img,
          data: JSON.parse(size)
        });
      }
    }
  }
};
</script>

<style lang="scss">
.appliance {
  background-color: #eee;
  padding-top: 10px;
}
.app-holder {
  display: flex;
  flex-wrap: wrap;
  div {
    width: 280px;
    h4 {
      margin: 0px;
      padding: 0px;
    }
  }
  div:nth-child(1) {
    height: 200px;
    overflow: auto;
  }
  .list-holder {
    a {
      display: block;
      padding: 5px 5px;
      background: #ccc;
      border-bottom: 1px solid #eee;
      border-top: 1px solid #ddd;
      color: #555;
      text-decoration: none;
      text-transform: capitalize;
      &:hover {
        background: #eee;
        color: #000;
      }
    }
  }
}
</style>
