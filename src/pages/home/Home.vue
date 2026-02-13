<template>
  <q-page>
    <!-- Seção de Apresentação -->
    <div class="q-pa-xl">
      <div class="row justify-center items-center q-gutter-md">
        <q-img
          class="image"
          src="../../assets/imagem-perfil.jpeg"
          spinner-color="white"
          style="height: 140px; max-width: 150px; border-radius: 100px"
        />
        <div class="name text-center">
          Olá, eu sou o <br />
          Alison Reisen Cordeiro
        </div>
      </div>
    </div>

    <!-- Seção Quem Sou -->
    <div class="q-pa-xl">
      <div class="container_introduct text-center">Quem Sou?</div>

      <div class="row justify-center">
        <div class="intro_text q-mt-md col-12 col-md-8">
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
    </div>

    <!-- Habilidades Técnicas -->
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
            <div class="skill-name q-mt-sm">{{ skill.name }}</div>
          </div>
        </q-card>
      </div>
    </div>

    <!-- Especialização ERP -->
    <div class="q-pa-xl">
      <div class="row justify-center">
        <q-card
          class="erp-card text-white shadow-10 col-12 col-md-8"
          style="border-left: 4px solid burlywood"
        >
          <q-card-section>
            <div class="text-h6 text-burlywood flex items-center">
              <q-icon name="mdi-briefcase-check" class="q-mr-sm" size="28px" />
              Especialista em ERPs & Regra de Negócio
            </div>
            <div class="text-body1 q-mt-md" style="opacity: 0.9">
              Experiência sólida com <strong>TOTVS RM</strong> (Foco em TAF e
              Integrações SQL) e <strong>Winthor</strong>. Atuação na resolução
              de conflitos de serviços, criação de relatórios complexos e
              sustentação de sistemas críticos.
            </div>
          </q-card-section>
        </q-card>
      </div>
    </div>

    <!-- Projetos -->
    <div class="q-pa-xl">
      <div class="cases-title q-mb-lg">Projetos</div>
      <div class="row justify-center q-gutter-md">
        <q-card
          v-for="project in projects"
          :key="project.title"
          style="background: #183447"
          class="text-white col-12 col-sm-5 col-md-3"
        >
          <q-card-section>
            <div class="text-h6">{{ project.title }}</div>
            <div class="text-subtitle2 q-mt-xs">{{ project.tech }}</div>
            <div class="text-body2 q-mt-sm">{{ project.description }}</div>
          </q-card-section>

          <q-card-actions>
            <q-btn
              flat
              icon="mdi-git"
              :href="project.link"
              target="_blank"
              label="Ver Projeto"
              color="#e6b873

"
            >
              <q-tooltip>Visualizar no GitHub</q-tooltip>
            </q-btn>
          </q-card-actions>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<script setup lang="ts">
import { Images } from "../../assets/index";
const skills = [
  { name: "Vue.js", icon: "mdi-vuejs" },
  { name: "Quasar", icon: "mdi-lightning-bolt" },
  { name: "HTML", icon: "mdi-language-html5" },
  { name: "CSS", icon: "mdi-language-css3" },
  //{ name: "Node.js", icon: "mdi-nodejs" },
  { name: "Python", icon: "mdi-language-python" },
  { name: "FastAPI", icon: "mdi-api" },

  { name: "Oracle", icon: "mdi-database" },
  { name: "SQL Server", icon: "mdi-database" },
  { name: "MySQL", icon: "mdi-database" },
  { name: "JasperReports", icon: "mdi-file-chart" },
  { name: "Power BI", icon: "mdi-chart-bar" },
  { name: "Git", icon: "mdi-git" },
  { name: "API REST", icon: "mdi-api" },
];

const projects = [
  {
    title: "Portfólio",
    tech: "Vue.js + Quasar",
    description:
      "Aplicação web desenvolvida com Vue.js e Quasar, focada em performance, responsividade e arquitetura baseada em componentes. Interface moderna e organizada para apresentação profissional de projetos e habilidades.",
    img: null,
  },

  {
    title: "Jokenpô API Serverless",
    tech: "Python + FastAPI",
    description:
      "API RESTful desenvolvida com FastAPI, evoluída de um script local para uma aplicação serverless. Implementa validação de dados, documentação automática via Swagger e deploy em ambiente cloud, garantindo escalabilidade e disponibilidade global.",
    link: "https://www.reisen.app.br/docs",
    img: null,
  },
];
</script>

<style>
.q-page {
  background: linear-gradient(180deg, #0e2a38 0%, #123f54 100%);
  font-family: "Inter", sans-serif;

  min-height: 100vh;
}

.image {
  border-radius: 50%;
  border: 3px solid #e6b873;
  transition: transform 0.3s ease;
}

.image:hover {
  transform: scale(1.05);
}

.name {
  font-size: 28px;
  font-family: Arial, Helvetica, sans-serif;
  color: #e6b873;
  font-weight: bold;
  line-height: 1.4;
}

.container_introduct,
.skills-title,
.cases-title {
  font-size: 36px;
  font-weight: bold;
  text-align: center;
  color: #e6b873;
  margin-bottom: 20px;
}

.intro_text {
  color: #f5f5f5;
  font-size: 17px;
  line-height: 1.8;
  max-width: 750px;
  margin: 0 auto;
  text-align: center;
}

.skill-card {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  background: #162a3a;

  color: #e6b873;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.25);

  transition: all 0.3s ease;
}

.skill-card:hover {
  transform: translateY(-6px) scale(1.05);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.45);
}

.skill-name {
  font-size: 14px;
  font-weight: 600;
}

.q-card {
  border-radius: 14px;
  transition: all 0.3s ease;
}

.q-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.4);
}

.bg-grey-10 {
  border-radius: 14px;
  backdrop-filter: blur(6px);
}
.erp-card {
  background: #162f40;
  border-radius: 16px;
  border-left: 4px solid #e6b873;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.25);
}

@media (max-width: 768px) {
  .name {
    font-size: 22px;
    text-align: center;
  }

  .container_introduct,
  .skills-title,
  .cases-title {
    font-size: 28px;
  }

  .intro_text {
    font-size: 15px;
    padding: 0 10px;
  }

  .skill-card {
    width: 100px;
    height: 100px;
  }
}
</style>
