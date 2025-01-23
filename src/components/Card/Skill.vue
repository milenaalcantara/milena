<script lang="ts">
import { defineComponent, type PropType } from 'vue';
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { type IconDefinition } from '@fortawesome/fontawesome-common-types';
import { faLinkedin } from "@fortawesome/free-brands-svg-icons";

export default defineComponent({
  name: "CardSkill",
  props: {
    icon: {
        type: Object as PropType<IconDefinition>,
        required: true
    },
    name: {
        type: String,
        required: true
    }
  }
})
</script>

<template>
    <div class="container">
        <FontAwesomeIcon :icon="icon" class="icon"/>
        <span class="name">{{ name }}</span>
    </div>
</template>

<style scoped>
.container {
  display: flex;
  padding: 24px;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 32px;
  border-radius: 4px;
  border: 2px solid #000000;
  background-color: #FFFFFF;
  transition: .3s;
  
  text-align: center;
  font-size: 20px;
  font-style: normal;
  font-weight: 700;
  line-height: 24px;
  letter-spacing: -0.4px;
  text-transform: capitalize;
}

.container:hover {
  background-color: #000000;
}

.icon {
  font-size: 56px;
  color: #000000;
}

.name {
  color: #000000;
  text-align: center;
  font-size: 20px;
  font-style: normal;
  font-weight: 700;
  line-height: 24px;
  letter-spacing: -0.4px;
  text-transform: capitalize;
} 
</style>