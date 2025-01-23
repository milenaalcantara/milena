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

<style scoped>
h1 {
  font-size: 48px;
  font-style: normal;
  font-weight: 400;
  line-height: 56px;
  letter-spacing: -0.96px;
  margin-bottom: 60px;
}


</style>
