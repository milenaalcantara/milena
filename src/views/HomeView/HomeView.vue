<script lang="ts">
import { defineComponent } from "vue";
import { CardMode } from "../../models/card";
import AboutView from "../AboutView.vue";
import Section from "../../components/Card/Section.vue";
import Presentation from "./Sections/Presentation.vue";

export default defineComponent({
  name: "HomeView",
  components: {
    Section,
  },
  data() {
    return {
      sections: [
        {
          firstTitle: "",
          lastTitle: "",
          mode: CardMode.LIGHT,
          content: Presentation,
        },
        {
          firstTitle: "My",
          lastTitle: "Skills",
          mode: CardMode.LIGHT,
          content: AboutView,
        },
        {
          firstTitle: "My",
          lastTitle: "Experience",
          mode: CardMode.DARK,
          content: AboutView,
        },
        {
          firstTitle: "About",
          lastTitle: "Me",
          mode: CardMode.LIGHT,
          content: AboutView,
        },
        {
          firstTitle: "My",
          lastTitle: "Projects",
          mode: CardMode.DARK,
          content: AboutView,
        },
        {
          firstTitle: "My",
          lastTitle: "Testimonial",
          mode: CardMode.LIGHT,
          content: AboutView,
        },
        {
          firstTitle: "",
          lastTitle: "",
          mode: CardMode.LIGHT,
          content: AboutView,
        },
      ],
    };
  },
});
</script>

<template>
  <main>
    <Section v-for="section in sections" :key="section" :mode="section.mode">
      <template #title>
        <h1>
          {{ section.firstTitle }} <b>{{ section.lastTitle }}</b>
        </h1>
      </template>
      <template #content>
        <component :is="section.content" />
      </template>
    </Section>
  </main>
</template>
