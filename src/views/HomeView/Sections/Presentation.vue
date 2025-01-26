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
  <div class="w-full max-w-7xl flex flex-col-reverse md:flex-row justify-center items-center">
    <div class="flex flex-col my-[20px] xl:mt-40">
      <h1 class="text-black text-5xl leading-[56px] font-normal tracking-[-0.96px] mb-[12px]">Olá, eu sou a <b class="font-extrabold">Milena.</b></h1>
      <h1 class="text-black text-5xl leading-[56px] tracking-[-0.96px] font-extrabold">Software <span class="text-white text-outside">Developer</span></h1>
      <p class="font-normal text-[#71717A] tracking-[0.32px] leading-6 text-base mt-8">
        Eu sou a Milena Alcântara, uma desenvolvedora de software de
        Fortaleza-CE. Atuo no desenvolvimento front-end web e mobile. Alumni do Apple Developer Academy.
      </p>
      <div class="flex flex-row gap-8 mt-[57px]">
        <a 
          href="" 
          class="text-2xl py-4 px-5 bg-white hover:bg-black border-2 rounded border-black text-black hover:text-white transition duration-0 hover:duration-300"
        >
          <FontAwesomeIcon :icon="linkedinIcon" />
        </a>
        <a 
          href="" 
          class="text-2xl py-4 px-5 bg-white hover:bg-black border-2 rounded border-black text-black hover:text-white transition duration-0 hover:duration-300"
        >
          <FontAwesomeIcon :icon="githubIcon" />
        </a>
      </div>
    </div>
    <img
      src="../../../assets/images/girl-banner.svg"
      alt="Girl Banner"
      class="w-full min-w-[343px]"
    />
  </div>
</template>

<style scoped>
.text-outside {
  text-shadow: -2px -2px 0 black, 2px -2px 0 black, -2px 2px 0 black,
    2px 2px 0 black, -2px 0px 0 black, 2px 0px 0 black, 0px -2px 0 black,
    0px 2px 0 black;
}
</style>
