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
  <section class="w-full py-[92px] px-[100px] flex flex-col justify-center items-center" :style="cardStyle">
    <slot name="title"></slot>
    <slot name="content" class="content"></slot>
  </section>
</template>
