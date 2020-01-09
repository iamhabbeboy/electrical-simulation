<template>
  <div class="pole-holder">
    <div>
      <img :src="require(`../assets/${url}.svg`)" width="50" height="50" />
    </div>
    <div>
      <div class="pole-wire">&nbsp;</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    url: {
      type: String,
      required: true
    }
  },
  mounted() {
    // this.url = 
  }
};
</script>
