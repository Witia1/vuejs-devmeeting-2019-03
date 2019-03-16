<template>
<div>
<div
     v-for="option of voteOptions"
     :key="option"
     >
  <BaseButton
              variant="text"
              :label="option.text"
              />
  </div>
  </div>
</template>


<script>
  import BaseButton from "@/components/BaseButton.vue";
  
  export default {
    name: 'VoteOptions',
    components: {
      BaseButton
    },    
    data: () => ({
      voteOptions: [
        {
          id: 1,
          text: 'Tak',
        },
        {
          id: 2,
          text: 'Nie wiem',
        },
        {
        id: 3,
        text: 'Nie',
        },
      ],
    }),
  };
</script>