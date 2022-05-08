<template>
  <span :class="`badge bg-${color} m-1`">{{ text.toUpperCase() }}</span>
</template>

<script>
export default {
  props: {
    color: {
      type: String,
      default: "primary",
    },
    text: {
      type: String,
      required: true,
    },
  },
};
</script>
