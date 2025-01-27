<script lang="ts">
import { defineComponent } from "vue";
import { CardMode } from "../../models/card";
import Section from "../../components/Card/Section.vue";
import Presentation from "./Sections/Presentation.vue";
import Skills from "./Sections/Skills.vue";
import AboutMe from "./Sections/AboutMe.vue";
import Projects from "./Sections/Projects.vue";
// import Contact from "./Sections/Contact.vue";

export default defineComponent({
  name: "HomeView",
  components: {
    Section
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
          firstTitle: "Minhas",
          lastTitle: "Skills",
          mode: CardMode.DARK,
          content: Skills,
        },
        {
          id: 3,
          firstTitle: "",
          lastTitle: "",
          mode: CardMode.LIGHT,
          content: AboutMe,
        },
        {
          id: 4,
          firstTitle: "Meus",
          lastTitle: "Projetos",
          mode: CardMode.DARK,
          content: Projects,
        },
      ],
    };
  },
});
</script>

<template>
  <main>
    <Section v-for="section in sections" :key="section.id" :mode="section.mode">
      <template v-if="section.firstTitle !== ''" #title>
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
