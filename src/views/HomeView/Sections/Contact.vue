<script lang="ts">
import { defineComponent } from "vue";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { faGithubSquare, faLinkedin } from "@fortawesome/free-brands-svg-icons";

export default defineComponent({
  name: "Contact",
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
  <div class="w-full flex flex-col-reverse justify-center items-center xl:flex-row">
    <form action="" method="post" class="flex flex-col item-left gap-[20px] xl:pr-[108px]">
      <input type="text" name="name" value="" placeholder="Nome" class="h-[56px] w-full border-2 rounded px-[24px] py-[18px]">
      <input type="text" name="email" value="" placeholder="E-mail" class="h-[56px] w-full border-2 rounded px-[24px] py-[18px]">
      <input type="text" name="answer" value="" placeholder="Como posso te ajudar?" class="h-[56px] w-full border-2 rounded px-[24px] py-[18px]">
      <div class="flex flex-row gap-8 mt-[57px]">
        <button type="submit" class="h-[56px] w-full py-[16px] px-[20px] border-2 rounded px-[24px] py-[18px] bg-black hover:bg-gray-900 text-white">
          Enviar
        </button>
        <a 
          href="https://www.linkedin.com/in/milimaalc/" 
          target="_blank"
          class="flex p-[16px] justify-center items-center text-[20px] h-[56px] w-[56px] bg-white hover:bg-black border-2 rounded border-black text-black hover:text-white transition duration-0 hover:duration-300"
        >
          <FontAwesomeIcon :icon="linkedinIcon" />
        </a>
        <a 
          href="https://github.com/milenaalcantara" 
          target="_blank"
          class="flex p-[16px] text-[20px] h-[56px] w-[56px] justify-center items-center bg-white hover:bg-black border-2 rounded border-black text-black hover:text-white transition duration-0 hover:duration-300"
        >
          <FontAwesomeIcon :icon="githubIcon" />
        </a>
      </div>
    </form> 

    <div class="w-full flex flex-col justify-center items-center">
      <h1 class="text-black text-5xl leading-[56px] tracking-[-0.96px] font-extrabold">Me envie uma mensagem</h1>
      <p>Tem uma pergunta ou proposta, ou apenas quer dizer olá? Vá em frente.</p>
    </div>
  </div>
</template>

