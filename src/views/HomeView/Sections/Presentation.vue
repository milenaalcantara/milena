<script lang="ts">
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { faGithubSquare, faLinkedin } from "@fortawesome/free-brands-svg-icons";
import { defineComponent } from "vue";

export default defineComponent({
  name: "Presentation",
  components: {
    FontAwesomeIcon,
  },
  data() {
    return {
      linkedinIcon: faLinkedin,
      githubIcon: faGithubSquare,
    };
  },
});
</script>

<template>
  <div class="content">
    <div class="text-group">
      <div class="text-line">
        <span class="text">Olá, eu sou a</span>
        <span class="text text-strong">Milena.</span>
      </div>
      <div class="text-line">
        <span class="text text-strong">Software</span>
        <span class="text text-outside">Developer</span>
      </div>
      <p class="description">
        Eu sou a Milena Alcântara, uma desenvolvedora de software de
        Fortaleza-CE. Atuo no desenvolvimento front-end web e mobile, formada em
        desenvolvimento iOS pela Apple Developer Academy. Gosto de aplicações
        utilitárias.
      </p>
      <div class="social-group">
        <a href="" class="social"><FontAwesomeIcon :icon="linkedinIcon" /></a>
        <a href="" class="social"><FontAwesomeIcon :icon="githubIcon" /></a>
      </div>
    </div>
    <img
      src="../../../assets/images/girl-banner.svg"
      alt="Girl Banner"
      class="banner"
    />
  </div>
</template>

<style scoped>
.content {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  max-width: 1280px;
}

.text-group {
  display: flex;
  flex-direction: column;
  max-width: 600px;
  margin: 165px auto 0 0;
}

.text-line {
  display: flex;
  flex-direction: row;
  gap: 14px;
}

.text {
  color: #000000;
  font-size: 48px;
  line-height: 56px;
  font-weight: 400;
  letter-spacing: -0.96px;
}

.text-strong {
  font-weight: 800;
}

.text-outside {
  font-weight: 800;
  color: #ffffff;
  text-shadow: -2px -2px 0 black, 2px -2px 0 black, -2px 2px 0 black,
    2px 2px 0 black, -2px 0px 0 black, 2px 0px 0 black, 0px -2px 0 black,
    0px 2px 0 black;
}

.description {
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  letter-spacing: 0.32px;
  margin-top: 32px;
  color: #71717a;
}

.social-group {
  display: flex;
  flex-direction: row;
  gap: 32px;
  padding: 4px 0px;
  margin-top: 115px;
}

.social {
  font-size: 24px;
  padding: 12px 16px;
  background-color: #ffffff;
  color: #000000;
  border: 3px solid #000000;
  border-radius: 4px;
  text-decoration: none;
}

.social:hover {
  background-color: #000000;
  color: #ffffff;
}

img {
  height: max-content;
  width: max-content;
}
</style>
