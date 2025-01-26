<script lang="ts">
import { CardMode } from "../../models/card";
import { defineComponent, type PropType } from "vue";

export default defineComponent({
  name: "Section",
  props: {
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
  <section class="w-full px-[16px] py-[40px] xl:py-[92px] xl:px-[100px] flex flex-col justify-center items-center" :style="cardStyle">
    <slot name="title"></slot>
    <slot name="content" class="content"></slot>
  </section>
</template>
