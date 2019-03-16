<template>
  <div class="vote">
    <h1>Vote</h1>
    <VoteOptions/>
  </div>
</template>

<script>
  import VoteOptions from "@/components/VoteOptions.vue";

  export default {
    name: "vote",
    components: {
      VoteOptions
    }
  };
</script>
