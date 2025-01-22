<script lang="ts">
import { CardMode } from "../../models/card";
import { defineComponent, type PropType } from "vue";

export default defineComponent({
  name: "Section",
  props: {
    firstTitle: {
      type: String,
    },
    lastTitle: {
      type: String,
    },
    mode: {
      type: Number as PropType<CardMode>,
      required: true,
    },
  },
  computed: {
    cardStyle() {
      return {
        backgroundColor: this.mode === CardMode.LIGHT ? "#FFFFFF" : "#000000",
        color: this.mode === CardMode.LIGHT ? "#000000" : "#FFFFFF",
      };
    },
  },
});
</script>

<template>
  <section class="container" :style="cardStyle">
    <slot name="title" class="title"></slot>
    <slot name="content" class="content"></slot>
  </section>
</template>

<style scoped>
.container {
  width: 100vw;
  padding: 60px 80px;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.title > h1 {
  font-weight: normal;
  font-size: 56px;
}
</style>
