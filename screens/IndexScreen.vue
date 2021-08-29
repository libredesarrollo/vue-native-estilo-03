<template>
  <view :style="style.container">
    <text :style="[style.h1, , { backgroundColor: bg }, {borderColor:'yellow'}, {borderWidth: 10 }]">Index</text>
    <text :style="style.h3">Bloque de texto secundario</text>
    <button title="Ir a Detail" @press="goToDetail"></button>
  </view>
</template>
<script>
import { style } from "../helpers/style";

export default {
  data() {
    return {
      style,
      bg:"blue"
    };
  },
  props: {
    navigation: {
      Object,
    },
  },
  methods: {
    goToDetail: function () {
      
      this.navigation.navigate("Detail");
    },
  },
};
</script>