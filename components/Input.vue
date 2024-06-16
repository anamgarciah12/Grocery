<template>
  <v-text-field
    :label="label"
    :dark="dark"
    :rules="rules"
    v-model="localModel"
    rounded
    :style="width && `max-width:${width}`"
    outlined
    :hideDetails="hideDetails"
    :prependInnerIcon="prependInnerIcon && `mdi-${prependInnerIcon}`"
    dense
  />
</template>

<script>
export default {
  props: {
    prependInnerIcon: {
      type: String,
      default: "",
    },
    model: {
      type: [String, Number],
      default: null,
    },
    hideDetails: {
      type: Boolean,
      default: false,
    },
    label: {
      type: String,
      default: "Label",
    },
    rules: {
      type: Array,
      default: () => [],
    },
    dark: {
      type: Boolean,
      default: false,
    },
    width: {
      type: String,
      default: "",
    },
  },
  data() {
    return {
      localModel: null,
    };
  },
  watch: {
    localModel(val) {
      this.$emit("update:model", val);
    },
    model(val) {
      this.localModel = val;
    },
  },
};
</script>
