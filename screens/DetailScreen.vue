<template>
  <view :style="style.container">
    <text :style="style.h1">Detail</text>
    <text :style="style.h3">Bloque de texto secundario</text>
    <button title="Ir a Index" @press="goToIndex"></button>
  </view>
</template>
<script>

import { style } from "../helpers/style"

export default {
  data() {
    return {
      style,
    };
  },
  props: {
    navigation: {
      Object,
    },
  },
  methods: {
    goToIndex: function () {
      this.navigation.navigate("Index");
    },
  },
};
</script>
