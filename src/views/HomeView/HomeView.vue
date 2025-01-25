<script lang="ts">
import { defineComponent } from "vue";
import { CardMode } from "../../models/card";
import AboutView from "../AboutView.vue";
import Section from "../../components/Card/Section.vue";
import Presentation from "./Sections/Presentation.vue";
import Skills from "./Sections/Skills.vue";

export default defineComponent({
  name: "HomeView",
  components: {
    Section,
  },
  data() {
    return {
      sections: [
        {
          id: 1,
          firstTitle: "",
          lastTitle: "",
          mode: CardMode.LIGHT,
          content: Presentation,
        },
        {
          id: 2,
          firstTitle: "My",
          lastTitle: "Skills",
          mode: CardMode.LIGHT,
          content: Skills,
        },
        {
          id: 3,
          firstTitle: "My",
          lastTitle: "Experience",
          mode: CardMode.DARK,
          content: AboutView,
        },
        {
          id: 4,
          firstTitle: "About",
          lastTitle: "Me",
          mode: CardMode.LIGHT,
          content: AboutView,
        },
        {
          id: 5,
          firstTitle: "My",
          lastTitle: "Projects",
          mode: CardMode.DARK,
          content: AboutView,
        },
        {
          id: 6,
          firstTitle: "My",
          lastTitle: "Testimonial",
          mode: CardMode.LIGHT,
          content: AboutView,
        },
        {
          id: 7,
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
    <Section v-for="section in sections" :key="section.id" :mode="section.mode">
      <template #title>
        <h1 class="font-normal tracking-[-0.96px] leading-[56px] text-5xl text-center capitalize mb-[60px]">
          {{ section.firstTitle }} <b>{{ section.lastTitle }}</b>
        </h1>
      </template>
      <template #content>
        <component :is="section.content" />
      </template>
    </Section>
  </main>
</template>
