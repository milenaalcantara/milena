<script lang="ts">
import { defineComponent } from 'vue';
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
    faBootstrap
} from "@fortawesome/free-brands-svg-icons";
import Skill from '../../../components/Card/Skill.vue';

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
                    name: ""
                },
                {
                    id: 2,
                    icon: faSwift,
                    name: ""
                },
                {
                    id: 3,
                    icon: faAppStoreIos,
                    name: ""
                },
                {
                    id: 4,
                    icon: faHtml5,
                    name: ""
                },
                {
                    id: 5,
                    icon: faCss3,
                    name: ""
                },
                {
                    id: 6,
                    icon: faJs,
                    name: ""
                },
                {
                    id: 7,
                    icon: faVuejs,
                    name: ""
                },
                {
                    id: 8,
                    icon: faReact,
                    name: ""
                },
                {
                    id: 9,
                    icon: faSass,
                    name: ""
                },
                {
                    id: 10,
                    icon: faFigma,
                    name: ""
                }
            ]
        }
    }
})
</script>

<template>
    <div class="container">
        <Skill v-for="skill in skills" :key="skill.id" :icon="skill.icon" :name="skill.name"/>
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