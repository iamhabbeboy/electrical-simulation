<template>
  <div>
    <div style="float:left">
    <h1>Simulation</h1>
    </div>
    <div style="float:right">
      <br/>
      You need such inverter,<br />
      <a href="#">Contact Us </a> / <a href="#">Feedback </a>
    </div>
    <div style="clear:both;"></div>
    <div class="simulator">
      <div class="inner-simulator">
        <div style="padding-bottom: 10px;padding-top: 10px;">
          <h3 style="text-align:center">Simulator Box</h3>
        </div>
        <div class="simulator-box" v-if="appliances.length">
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
        <div class="simulator-battery">
          <img
            src="../assets/inverter.svg"
            width="100"
            style="position: relative;bottom: 20px;"
          />
        </div>
      </div>
       <div class="button-placeholder">
        <button class="refresh" @click="refresh">
          <img
            src="../assets/refresh.svg"
            width="13"
            style="position: relative;top: 3px;"
          />&nbsp;Refresh
        </button>
        <button class="save" @click="save" disabled>
          <img
            src="../assets/upload.svg"
            width="13"
            style="position: relative;top: 3px;"
          />&nbsp;Save
        </button>
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
  },
  methods: {
    refresh() {
      if (window.confirm("Are you sure ?")) {
        EventBus.$off("ADD");
        EventBus.$off("WATT");
        this.appliances = [];
      }
    },
    save() {}
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

.simulator-battery {
  clear: both;
  border-top: 3px solid orange;
  margin-bottom: 5px;
}

.button-placeholder {
  display: flex;
  align-items: center;
  justify-content: center;
  margin: auto;
  text-align: center;
}
button {
  padding: 10px 30px;
  border: transparent;
  margin-bottom: 15px;
  margin-left: 10px;
  margin-right: 10px;
  font-weight: bold;
  font-size: 14px;
  border-radius: 5px;
  cursor: pointer;
  transition: 0.3s all;
  &:hover {
    opacity: 0.7;
  }
  &.refresh {
    background: #cce5ff;
  }
  &.save {
    background-color: #d4edda;
  }
}

</style>
