<script lang="ts">
import { defineComponent } from "vue";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import {
  faGitAlt,
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
    FontAwesomeIcon,
    Skill
  },
  data() {
    return {
      skills: [
        {
          id: 1,
          icon: faGitAlt,
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
  <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 gap-y-10 gap-x-[70px]">
    <Skill
      v-for="skill in skills"
      :key="skill.id"
      :icon="skill.icon"
      :name="skill.name"
    />
  </div>
</template>
