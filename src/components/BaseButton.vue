<template>
  <button class="button"
    :class="[loading ? 'loading' : '', variant]"
    v-bind="$attrs"
    v-on="$listeners"
    >
    <slot>
      {{ label }}
    </slot>
  </button>
</template>

<script>
  const buttonTypes = ['text', 'icon'];
  export default {
    name: 'BaseButton',
    inheritAttrs: false,
    props: {
      loading: {
        type: Boolean,
        required: false,
        default: 'test',
      },
      variant: {
        type: String,
        required: true,
        validator: value => buttonTypes.indexOf(value) !== -1,
      },
      label: {
        type: String,
        required: false,
        default: '',
      }
    }
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .loading {
    background-color: blue;
    color: white;
    border: none;
    border-radius: 5px;
    padding: 10px 15px;
    margin: 15px;
  }
</style>
