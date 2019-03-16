<template>
  <div class="home">
    <h1>Home</h1>
    <BaseButton
      label="Submit"
      @click="submit()"
  />
  </div>
</template>

<script>
import BaseButton from "@/components/BaseButton.vue";

export default {
  name: "home",
  components: {
    BaseButton
  }
};
</script>
