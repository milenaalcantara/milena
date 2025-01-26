<script lang="ts">
import { defineComponent, type PropType } from "vue";
import { type IconDefinition } from "@fortawesome/fontawesome-common-types";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";

export default defineComponent({
  name: "CardSkill",
  props: {
    icon: {
      type: Object as PropType<IconDefinition>,
      required: true,
    },
    name: {
      type: String,
      required: true,
    },
  },
  components: {
    FontAwesomeIcon,
  },
  mounted() {
    console.log(this.icon);
  },
});
</script>

<template>
  <div
    class="flex flex-col max-w-[186px] max-h-[186px] min-w-[160px] min-h-[160px] gap-8 justify-center items-center rounded border-2 border-white bg-black transition duration-0 hover:duration-300 hover:bg-white text-white hover:text-black"
  >
    <FontAwesomeIcon :icon="icon" class="text-[56px]" />
    <span
      class="w-full font-bold leading-6 text-sm text-center tracking-[-0.4px] capitalize"
    >
      {{ name }}
    </span>
  </div>
</template>
