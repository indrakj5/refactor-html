<template>
  <button type="button" :class="`btn btn-${type}`">
    {{ label }}
  </button>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      defaults: ""
    },
    type: {
      type: String,
      defaults: "primary"
    }
  }
};
</script>
