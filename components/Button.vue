<template>
  <v-btn
    :absolute="absolute"
    :right="right"
    :top="top"
    :block="block"
    :icon="icon !== '' ? true : false"
    :type="type"
    :disabled="disabled"
    v-bind="attrs"
    v-on="on"
    :color="color"
    @click="$emit('eventClick')"
    rounded
  >
    <span v-if="!icon">
      {{ label }}
    </span>
    <v-icon v-else> mdi-{{ icon }} </v-icon>
  </v-btn>
</template>

<script>
export default {
  props: {
    type: {
      type: String,
      default: "button",
    },
    block: {
      type: Boolean,
      default: false,
    },
    absolute: {
      type: Boolean,
      default: false,
    },
    on: {
      type: Object,
      default: () => {},
    },
    attrs: {
      type: Object,
      default: () => {},
    },
    top: {
      type: Boolean,
      default: false,
    },
    right: {
      type: Boolean,
      default: false,
    },
    color: {
      type: String,
      default: "primary",
    },
    icon: {
      type: String,
      default: "",
    },
    label: {
      type: String,
      default: "Label",
    },
    disabled: {
      type: Boolean,
      default: false,
    },
  },
};
</script>
