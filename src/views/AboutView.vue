<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "About",
});
</script>

<template>
  <div class="about">
    <h1 class="border-2">This is an about page</h1>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    display: flex;
    align-items: center;
  }
}
</style>
