<script lang="ts">
import { defineComponent } from 'vue';
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { faShareFromSquare } from "@fortawesome/free-solid-svg-icons";
import { CardType } from '../../../models/card';
import AuralizeImage from "../../../assets/images/auralize.svg"
import FiveSensesImage from "../../../assets/images/five-senses.svg"
import QuietImage from "../../../assets/images/quiet.svg"
import HomeroImage from "../../../assets/images/homero.svg"
import MultilaserImage from "../../../assets/images/multi.svg"

export default defineComponent({
    name: "Projects",
    components: {
        FontAwesomeIcon,
    },
    data() {
        return {
            iconShare: faShareFromSquare,
            projects: [
                {
                    number: "01",
                    title: "Auralize",
                    description: "Auralize oferece acústica virtual para projetos arquitetônicos, com foco na simulação de ambientes sonoros virtuais e medições acústicas através do dispositivo móvel, permitindo que você ouça seu projeto antes de construí-lo. No Auralize pude participar em quase todas as áreas que ele abrange, back-end com python e Django, front-end web com React e aplicação mobile iOS com Swift, UIKit, AVFoundation e outras.",
                    imgUrl: AuralizeImage,
                    projectUrl: 'https://www.auralize.com.br/',
                    presentation: CardType.IMG_LEFT
                },
                {
                    number: "02",
                    title: "Quiet",
                    description:  "Quiet propõe uma experiência sensorial por meio de uma interface simples e imersiva. Nele você pode explorar os diferentes elementos da tela para interagir com os sons naturais cuidadosamente selecionados para oferecer a experiência relaxante de uma praia. Quiet foi projetado e desenvolvido para ser imersivo e acessível contando com haptics e animações, compatibilidade com VoiceOver, aumento de texto, zoom de tela e cores compatíveis com diferentes contrastes.",
                    imgUrl: QuietImage,
                    projectUrl: "https://github.com/milenaalcantara/Quiet",
                    presentation: CardType.IMG_RIGHT
                },
                {
                    number: "03",
                    title: "5Senses",
                    description: "O 5Senses é um app que tem como objetivo relaxar a mente em momentos de tensão utilizando uma prática de concentração plena chamada de 5 sentindos, onde você descreve itens para cada sentido do nosso corpo, como visão, audição, olfato, tato e paladar. Este app é indicado para pessoas que buscam o desvio de pensamentos intrusivos.",
                    imgUrl: FiveSensesImage,
                    projectUrl: "https://github.com/milenaalcantara/FiveSenses",
                    presentation: CardType.IMG_LEFT
                },
                {
                    number: "04",
                    title: "Homero",
                    description: "Homero é uma plataforma de ensino EAD com conteúdo personalizado. A plataforma tem a capacidade de detectar a melhor forma de entregar o conteúdo individualmente para cada aluno, assim tornando a experiência de ensino mais enriquecedora e única. Por meio de uma Inteligência Artificial, a plataforma avalia e considera o ritmo do aluno, seus conhecimentos prévios, os resultados de avaliações e a atenção dispensada no conteúdo já ministrado. Dentro da plataforma você terá ajuda do assistente virtual Homero, que fará com que a sua jornada de aprendizado seja facilitada ao atuar de forma ativa com apresentação do conteúdo, realização de perguntas e feedbacks.",
                    imgUrl: HomeroImage,
                    projectUrl: "https://homero.app.br/",
                    presentation: CardType.IMG_RIGHT
                },
                {
                    number: "05",
                    title: "Multilaser",
                    description: "O site de suporte da multi foi desenvolvido para que seus cliente encontrem as respostas para suas dúvidas e acesse detalhes sobre os produtos do grupo Multi em um só lugar. Disponibilizando manuais e drivers, dicas e soluções e permitindo solicitar o conserto de produtos, além de permitir acesso a área do revendedor. Nesse projeto atuei como front-end.",
                    imgUrl: MultilaserImage,
                    projectUrl: "https://suporte.grupomulti.com.br/",
                    presentation: CardType.IMG_LEFT
                },
            ]
        }
    },
})
</script>

<template>
    <div v-for="project in projects">
        <div 
            v-if="project.presentation === 'left'"
            class="w-full py-5 flex flex-col gap-[28px] xl:gap-[40px] items-center justify-start lg:flex-row min-w-[343px] max-w-[1216px]"
        >
            <div class="md:py-[39px] md:pr-[60px]">
                <img :src="project.imgUrl" alt="Imagem do Projeto" class="rounded-[18px] w-full md:max-w-[530px]">
            </div>
            <div class="flex flex-col gap-[28px] lg:max-w-[582px] items-start">
                <h1 class="text-white text-5xl leading-[56px] tracking-[-0.96px] font-extrabold">{{ project.number }}</h1>
                <h2 class="text-white text-[32px] leading-[40px] tracking-[-0.64px] font-bold">{{ project.title }}</h2>
                <p class="font-normal text-[#71717A] tracking-[0.32px] leading-6 text-base">{{ project.description }}</p>
                <a :href="project.projectUrl" class="text-xl text-white" target="_blank"><FontAwesomeIcon :icon="iconShare" /></a>
            </div>
        </div>

        <div 
            v-else
            class="w-full py-5 flex flex-col-reverse gap-[28px] xl:gap-[40px] items-center justify-start lg:flex-row min-w-[343px] max-w-[1216px]"
        >
            <div class="flex flex-col gap-[28px] lg:max-w-[582px] items-start">
                <h1 class="text-white text-5xl leading-[56px] tracking-[-0.96px] font-extrabold">{{ project.number }}</h1>
                <h2 class="text-white text-[32px] leading-[40px] tracking-[-0.64px] font-bold">{{ project.title }}</h2>
                <p class="font-normal text-[#71717A] tracking-[0.32px] leading-6 text-base">{{ project.description }}</p>
                <a :href="project.projectUrl" class="text-xl text-white" target="_blank"><FontAwesomeIcon :icon="iconShare" /></a>
            </div>
            <div class="md:py-[39px] md:pr-[60px]">
                <img :src="project.imgUrl" alt="Imagem do Projeto" class="rounded-[18px] w-full md:max-w-[530px]">
            </div>
        </div>
    </div>
</template>