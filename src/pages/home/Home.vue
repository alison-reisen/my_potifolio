<template>
  <q-page class="" style="background-color: #15658d">
    <q-page-container class="justify-content " style="display: flex;">
      <q-img
        class="image"
        src="../../assets/imagem-perfil.jpeg"
        spinner-color="white"
        style="height: 140px; max-width: 150px"
      />
      <div class="name">
        Olá, eu sou o <br />
        Alison Reisen Cordeiro
      </div>
    </q-page-container>

    <q-page-container>
      <div class="q-pl-md">
        <div class="container_introduct">Quem Sou?</div>

        <div class="intro_text q-mt-md q-px-lg">
          <p>
            Sou entusiasta por tecnologia, movido por curiosidade e pela vontade
            constante de evoluir. Tenho muitos sonhos e objetivos para o futuro,
            tanto pessoais quanto profissionais.
          </p>

          <p>
            Um deles é aprender a pilotar um avião — algo distante do que faço
            hoje, mas que representa meu interesse por desafios e aprendizado
            contínuo.
          </p>

          <p>
            Atualmente, sou graduando em
            <strong>Análise e Desenvolvimento de Sistemas</strong>, com previsão
            de conclusão em 2026.
          </p>

          <p>
            Busco construir uma carreira sólida na área de tecnologia, aplicando
            conhecimento técnico para resolver problemas reais e gerar valor por
            meio de soluções eficientes.
          </p>
        </div>
      </div>
    </q-page-container>

    <div class="q-pa-xl">
      <div class="skills-title q-mb-lg">Habilidades Técnicas</div>

      <div class="row justify-center q-gutter-lg">
        <q-card
          v-for="skill in skills"
          :key="skill.name"
          class="skill-card flex flex-center"
        >
          <div class="text-center">
            <q-icon :name="skill.icon" size="32px" />
            <div class="skill-name q-mt-sm">
              {{ skill.name }}
            </div>
          </div>
        </q-card>
      </div>
    </div>
    <div class="row justify-center q-mt-xl">
      <q-card
        class="bg-grey-10 text-white shadow-10"
        style="border-left: 4px solid burlywood; max-width: 800px; width: 100%"
      >
        <q-card-section>
          <div class="text-h6 text-burlywood flex items-center">
            <q-icon name="mdi-briefcase-check" class="q-mr-sm" size="28px" />
            Especialista em ERPs & Regra de Negócio
          </div>
          <div class="text-body1 q-mt-md" style="opacity: 0.9">
            Experiência sólida com <strong>TOTVS RM</strong> (Foco em TAF e
            Integrações SQL) e <strong>Winthor</strong>. Atuação na resolução de
            conflitos de serviços, criação de relatórios complexos e sustentação
            de sistemas críticos.
          </div>
        </q-card-section>
      </q-card>
    </div>

    <div class="q-pa-xl">
      <div class="cases-title q-mb-lg">Projetos</div>

      <div class="q-pa-md row justify-center q-gutter-md text-white ">
        <q-card
          v-for="project in projects"
          :key="project.title"
          style="background: radial-gradient(circle, #35a2ff 0%, #15658d 100%); max-width: 400px"
          class=""

        >
          <q-card-section>
            <div>
              <div class="text-h6">{{ project.title }}</div>
              <div class="text-subtitle2 q-mt-xs ">
                {{ project.tech }}
              </div>

              <div class="text-subtitle2">{{ project.description }}</div>
              <div class="project-img"><img :src="project.img" /></div>
            </div>
          </q-card-section>
          <div class="q-pa-md q-gutter-sm">
            <q-btn
              size="10px"

              icon="mdi-git"
              outline
              :href="project.link"
              target="_blank"
              label="Ir para o projeto"
            >
              <q-tooltip>Visualizar Projeto no repositorio do Git Hub</q-tooltip>
            </q-btn>
          </div>
        </q-card>
      </div>
    </div>

    <!--
    <q-page-container class="row q-gutter-md card">
      <q-card>
        <div>Projeto 1</div>
      </q-card>
      <q-card> <div>Projeto 2</div> </q-card>
    </q-page-container> -->
  </q-page>
</template>

<script setup lang="ts">
import { Images } from "../../assets/index";
const skills = [
  { name: "Vue.js", icon: "mdi-vuejs" },
  { name: "Quasar", icon: "mdi-lightning-bolt" },
  //  { name: 'Java Script', icon: 'mdi-Javascript' },
  // { name: 'HTML', icon: 'mdi-language-html5' },
  // { name: 'CSS', icon: 'mdi-language-css3' },
  // { name: 'Node.js', icon: 'mdi-nodejs' },
  // { name: 'NestJS', icon: 'mdi-hexagon-outline' },
  { name: "Oracle", icon: "mdi-database" },
  { name: "SQL Server", icon: "mdi-database" },
  { name: "MySQL", icon: "mdi-database" },
  { name: "JasperReports", icon: "mdi-file-chart" },
  { name: "Power BI", icon: "mdi-chart-bar" },
  { name: "Git", icon: "mdi-git" },
  // { name: 'API REST', icon: 'mdi-api' },
  // { name: 'WebSocket', icon: 'mdi-access-point' }
];

const projects = [
  {
    title: "Tech Reisen Portfólio",
    tech: "Vue.js + Quasar",
    description:
      "Este site! Desenvolvido com design responsivo, modo escuro e arquitetura baseada em componentes.",
    link: "https://github.com/alison-reisen/my_potifolio",
    img: null,
  },
  {
    title: "Tech Reisen Portfólio",
    tech: "Vue.js + Quasar",
    description:
      "Este site! Desenvolvido com design responsivo, modo escuro e arquitetura baseada em componentes.",
    link: "https://github.com/alison-reisen/my_potifolio",
    img: null,
  },
  {
    title: "Tech Reisen Portfólio",
    tech: "Vue.js + Quasar",
    description:
      "Este site! Desenvolvido com design responsivo, modo escuro e arquitetura baseada em componentes.",
    link: "https://github.com/alison-reisen/my_potifolio",
    img: null,
  },{
    title: "Tech Reisen Portfólio",
    tech: "Vue.js + Quasar",
    description:
      "Este site! Desenvolvido com design responsivo, modo escuro e arquitetura baseada em componentes.",
    link: "https://github.com/alison-reisen/my_potifolio",
    img: null,
  },{
    title: "Tech Reisen Portfólio",
    tech: "Vue.js + Quasar",
    description:
      "Este site! Desenvolvido com design responsivo, modo escuro e arquitetura baseada em componentes.",
    link: "https://github.com/alison-reisen/my_potifolio",
    img: null,
  },{
    title: "Tech Reisen Portfólio",
    tech: "Vue.js + Quasar",
    description:
      "Este site! Desenvolvido com design responsivo, modo escuro e arquitetura baseada em componentes.",
    link: "https://github.com/alison-reisen/my_potifolio",
    img: null,
  },
];
</script>

<style >


.container_name {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 25px;
}

.image {
  border-radius: 100px;
}

.name {
  font-size: 25px;
  font-family: Arial, Helvetica, sans-serif;
  color: burlywood;
  font-weight: bold;
  display: flex;
  padding-left: 50px;
}

.container_introduct {
  font-size: 42px;
  font-family: Arial, Helvetica, sans-serif;
  color: burlywood;
  font-weight: bold;
  display: flex;
  padding-left: 30%;
  padding-top: 50px;
}

.intro_text {
  color: #f5f5f5;
  font-size: 16px;
  line-height: 1.6;
  max-width: 700px;
}

.skill-card {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  background-color: #1e1e2f;
  color: burlywood;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
  transition: transform 0.3s ease;
}

.skill-card:hover {
  transform: scale(1.1);
}

.skill-name {
  font-size: 14px;
  font-weight: 600;
}

.skills-title {
  font-size: 36px;
  font-weight: bold;
  text-align: center;
  color: burlywood;
}

.cases-title {
  font-size: 36px;
  font-weight: bold;
  text-align: center;
  color: burlywood;
}
.my-card{
  max-width: 400px
}
</style>
