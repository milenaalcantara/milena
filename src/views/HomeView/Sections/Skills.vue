<script lang="ts">
import { defineComponent } from "vue";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import {
  faGit,
  faJs,
  faVuejs,
  faReact,
  faSass,
  faSwift,
  faAppStoreIos,
  faFigma,
  faHtml5,
  faCss3,
  faBootstrap,
} from "@fortawesome/free-brands-svg-icons";
import Skill from "../../../components/Card/Skill.vue";

export default defineComponent({
  name: "Skills",
  components: {
    Skill,
  },
  data() {
    return {
      skills: [
        {
          id: 1,
          icon: faGit,
          name: "Git",
        },
        {
          id: 2,
          icon: faSwift,
          name: "Swift",
        },
        {
          id: 3,
          icon: faAppStoreIos,
          name: "app store",
        },
        {
          id: 4,
          icon: faHtml5,
          name: "html5",
        },
        {
          id: 5,
          icon: faCss3,
          name: "css3",
        },
        {
          id: 6,
          icon: faJs,
          name: "JavaScript",
        },
        {
          id: 7,
          icon: faVuejs,
          name: "Vue",
        },
        {
          id: 8,
          icon: faReact,
          name: "React",
        },
        {
          id: 9,
          icon: faSass,
          name: "Sass",
        },
        {
          id: 10,
          icon: faFigma,
          name: "Figma",
        },
        {
          id: 11,
          icon: faBootstrap,
          name: "Bootstrap",
        },
      ],
    };
  },
});
</script>

<template>
  <div class="container">
    <div
      v-for="skill in skills"
      :key="skill.id"
      class="flex flex-col p-6 justify-center items-center gap-8 rounded border-2 border-black bg-white transition duration-0 hover:duration-300 hover:bg-black text-black hover:text-white"
    >
      <FontAwesomeIcon :icon="skill.icon" class="text-[56px]" />
      <span
        class="w-full font-bold leading-6 text-sm text-center tracking-[-0.4px] capitalize"
      >
        {{ skill.name }}
      </span>
    </div>
  </div>
</template>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 186px 186px 186px 186px 186px;
  grid-template-rows: 186px 186px;
  column-gap: 70px;
  row-gap: 40px;
}
</style>
