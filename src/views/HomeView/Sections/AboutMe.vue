<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: "AboutMe"
})
</script>

<template>
    <div class="w-full flex flex-col gap-[20px] md:flex-row md:gap-[88px]">
        <img src="../../../assets/images/girl-about.svg" alt="" class="w-full min-w-[343px]">
        <div class="flex flex-col">
            <h1 class="w-full text-left font-normal tracking-[-0.96px] leading-[56px] text-5xl text-center capitalize mb-[60px]">
                Sobre <b>Mim</b>
            </h1>
            <div class="flex flex-col gap-5">
                <p class="font-normal text-[#71717A] tracking-[0.32px] leading-6 text-base">
                    Sou uma desenvolvedora especializada em iOS e front-end web. 
                    Sou muito entusiasmada em dar vida aos aspectos técnicos e visuais de produtos digitais. 
                    Experiência do usuário e escrever código limpo, claro e legível são importantes para mim. 
                </p>
                <p class="font-normal text-[#71717A] tracking-[0.32px] leading-6 text-base">
                    Comecei minha jornada na tecnologia em 2017, quando ingressei no Bacharelado em Ciência da Computação 
                    no IFCE - Campus Maracanaú e, desde então, continuei a crescer e evoluir como desenvolvedora, 
                    assumindo novos desafios e aprendendo as tecnologias necessárias ao longo do caminho. Alumni 
                    do Apple Developer Academy, participei de diversos projetos engajantes colocando meu foco 
                    principal em front-end e mobile. Agora, alguns anos após começar minha jornada, sou capaz de 
                    construir aplicações usando tecnologias modernas como SwiftUI, React, Vue e muito mais.
                </p>
                <p class="font-normal text-[#71717A] tracking-[0.32px] leading-6 text-base">
                    Quando não estou no modo desenvolvedora, você pode me encontrar produzindo as mais diversas peças de crochê, 
                    desde um sousplat, roupas e até amigurumis, ou posso estar batendo fotos contemplando paisagens, lendo, 
                    assistindo e praticando atividades físicas, além de passar um tempo com a minha família.
                </p>
            </div>
        </div>
    </div>
</template>