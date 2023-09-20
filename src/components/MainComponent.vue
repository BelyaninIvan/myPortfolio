<template>
  <main class="content">
    <h2 class="content__title">Мои проекты</h2>
    <ul class="content__buttons-list">
      <li class="content__buttons-el">
        <MyButton
          @click="toggleStateVerstka"
        >
          Верстка
        </MyButton>
      </li>
      <li class="content__buttons-el">
        <MyButton
          @click="toggleStateReact"
        >
          React
        </MyButton>
      </li>
      <li class="content__buttons-el">
        <MyButton
          @click="toggleStateVue"
        >
            Vue.js
        </MyButton>
      </li>
      <li class="content__buttons-el">
        <MyButton
          @click="toggleStateDesign"
        >
            Макеты
        </MyButton>
      </li>
    </ul>
    <section class="content__lists">
      <ProjectsList v-if="isVerstka === true"
        :projectsList="verstka"
      >
      </ProjectsList>
      <ProjectsList v-if="isReact === true"
        :projectsList="react"
      >
      </ProjectsList>
      <ProjectsList v-if="isVue === true"
        :projectsList="vue"
      >
      </ProjectsList>
      <ProjectsList v-if="isDesign === true"
        :projectsList="design"
      >
      </ProjectsList>
    </section>
  </main>
</template>
<script>
import ProjectsList from '@/components/ProjectsList.vue';
export default {
  name: "MainComponent",
  components: {
    ProjectsList,
  },
  data() {
    return {
      verstka: [
        {
            id: 'v1',
            name: 'Светофор',
            img: 'src/assets/images/trafficLight.png',
            desc: 'Проект светофор. Лендинг транспортной компании',
            webLink: 'https://belyaninivan.github.io/trafficLights',
            codeLink: 'https://github.com/BelyaninIvan/trafficLights',
        },
        {
            id: 'v2',
            name: 'Magic Travel',
            img: 'src/assets/images/magicTravel.png',
            desc: 'Многостраничный сайт экскурсий по Саратову и области',
            webLink: 'https://belyaninivan.github.io/MagicTravel', 
            codeLink: 'https://github.com/BelyaninIvan/MagicTravel',
        },
        {
            id: 'v3',
            name: 'Saratov Tour',
            img: 'src/assets/images/saratovTour.png',
            desc: 'Многостраничный сайт о туристических маршрутах по городу Саратову',
            webLink: 'https://belyaninivan.github.io/SaratovTour', 
            codeLink: 'https://github.com/BelyaninIvan/SaratovTour',
        },
        {
            id: 'v4',
            name: 'Проект Место',
            img: 'src/assets/images/mesto.png',
            desc: 'Сайт с библиотекой фотографий, который имеет различный функционал',
            webLink: 'https://belyaninivan.github.io/ProjectMesto', 
            codeLink: 'https://github.com/BelyaninIvan/ProjectMesto',
        },
        {
            id: 'v5',
            name: 'Проект Uber',
            img: 'src/assets/images/uber.png',
            desc: 'Сайт для сервиса такси Uber',
            webLink: 'https://belyaninivan.github.io/bootstrap/', 
            codeLink: 'https://github.com/BelyaninIvan/bootstrap',
        },
      ],
      react: [
        {
          id: 'r1',
          name: 'Magic Travel',
          img: 'src/assets/images/MagicTravel.png',
          desc: 'Многостраничный сайт экскурсий по Саратову и области',
          webLink: 'https://belyaninivan.github.io/MagicTravel',
          codeLink: 'https://bitbucket.org/IvanBelyanin/jscourse/src/master/',
        },
        {
          id: 'r2',
          name: 'Frontera',
          img: 'src/assets/images/frontera.png',
          desc: 'Командный проект на стажировке по React',
          webLink: '',
          codeLink: '',
        },
      ],
      vue: [
        {
          id: 'vue1',
          name: 'GetWeather',
          img: 'src/assets/images/weather.png',
          desc: 'Сервис по предоставлению информации о погоде в каком-либо городе',
          webLink: 'https://belyaninivan.github.io/MagicTravel', // Исправить ссылку
          codeLink: 'https://github.com/BelyaninIvan/Vue_Weather',
        },
        {
          id: 'vue2',
          name: 'To-Do App',
          img: 'src/assets/images/toDoApp.png',
          desc: 'Приложения для отслеживания выполненных дел',
          webLink: 'https://belyaninivan.github.io/MagicTravel', // Исправить ссылку
          codeLink: 'https://github.com/BelyaninIvan/to-do_App',
        },
        {
          id: 'vue3',
          name: 'Photo Library',
          img: 'src/assets/images/photoLibrary.png',
          desc: 'Визитная карточка фотографа. Сервис для демонстрации работ',
          webLink: 'https://belyaninivan.github.io/MagicTravel', // Исправить ссылку
          codeLink: 'https://github.com/BelyaninIvan/photoLibrary',
        },
      ],
      design: [
        {
          id: 'm1',
          name: 'Saratov Tour',
          img: 'src/assets/images/saratovTour.png',
          desc: 'Разработанный макет к дипломной работе.',
          webLink: 'https://www.figma.com/file/WAXH54HoVGEyBJAcMTXJhL/Tokar-Mebel-%2B?type=design&node-id=0-1&mode=design&t=fCt2jx14TmRHcFr5-0',
          codeLink: '',
        },
        {
          id: 'm2',
          name: 'Magic travel',
          img: 'src/assets/images/magicTravel.png',
          desc: 'Разработанный макет к проекту "Magic Travel"',
          webLink: 'https://www.figma.com/file/WyzYmnJkNbkeKNgmzib42t/jscourse?type=design&node-id=0-1&mode=design&t=510rEifR9tFdatQA-0',
          codeLink: '',
        },
        {
          id: 'm3',
          name: 'Portfolio',
          img: 'src/assets/images/portfolio.png',
          desc: 'Разработанный макет к сайту-портфолио',
          webLink: 'https://www.figma.com/file/WyzYmnJkNbkeKNgmzib42t/jscourse?type=design&node-id=0-1&mode=design&t=510rEifR9tFdatQA-0',
          codeLink: '',
        },
      ],
      isVerstka: true,
      isReact: false,
      isVue: false,
      isDesign: false
    }
  },
  methods: {
    toggleStateVerstka() {
      this.isVerstka = true;
      this.isReact = false;
      this.isVue = false;
      this.isDesign = false;
    },
    toggleStateReact() {
      this.isVerstka = false;
      this.isReact = true;
      this.isVue = false;
      this.isDesign = false;
    },
    toggleStateVue() {
      this.isVerstka = false;
      this.isReact = false;
      this.isVue = true;
      this.isDesign = false;
    },
    toggleStateDesign() {
      this.isVerstka = false;
      this.isReact = false;
      this.isVue = false;
      this.isDesign = true;
    },
  },
}
</script>
<style scoped>
  .content {
    max-width: 1250px;
    margin: 0 auto; 
    padding: 50px 0 75px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    row-gap: 35px;
  }

  .content__title {
    margin: 0;
    padding: 0;
    color: #223146;
    font-size: 30px;
    font-weight: 900;
  }

  .content__buttons-list {
    max-width: 750px;
    margin: 0 auto;
    padding: 12px 40px;
    list-style-type: none;
    column-gap: 40px;

    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .content__lists {
    padding: 0 15px;
  }
</style>