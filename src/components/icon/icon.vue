<template>
  <component :is="iconName" />
</template>

<script>
import * as icons from "../../assets/icons";
console.log(icons);
export default {
  name: "Icon",

  setup() {
    return {};
  },

  components: {
    ...icons
  },

  props: {
    iconName: {
      required: true,
      type: String,
      validator(name) {
        return Object.keys(icons).includes(name);
      }
    }
  }
};
</script>

<style lang="scss" scoped></style>
