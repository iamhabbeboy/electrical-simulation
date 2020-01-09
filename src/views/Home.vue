<template>
  <div class="home">
    <Simulation />
    <Appliance />
  </div>
</template>

<script>
// @ is an alias to /src
import Appliance from "@/components/Appliances.vue";
import Simulation from "@/components/Simulation.vue";

export default {
  name: "home",
  components: {
    Simulation,
    Appliance
  }
};
</script>
