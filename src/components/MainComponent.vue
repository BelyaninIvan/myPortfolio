<template>
  <main class="content">
    <h2 class="content__title">Мои проекты</h2>
    <ul class="content__buttons-list">
      <li class="content__buttons-el">
        <MyButton>
          Верстка
        </MyButton>
      </li>
      <li class="content__buttons-el">
        <MyButton>
          React
        </MyButton>
      </li>
      <li class="content__buttons-el">
        <MyButton>
            Vue.js
        </MyButton>
      </li>
      <li class="content__buttons-el">
        <MyButton>
            Макеты
        </MyButton>
      </li>
    </ul>
    <section class="content__lists">
      <ProjectsList
        :projectsList="projects"
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
      projects: [
        {
            id: '1',
            name: 'Светофор',
            img: 'src/assets/images/trafficLight.png',
            desc: 'Проект светофор. Лендинг транспортной компании',
            webLink: 'https://belyaninivan.github.io/trafficLights',
            codeLink: 'https://github.com/BelyaninIvan/trafficLights',
        },
        {
            id: '2',
            name: 'Magic Travel',
            img: 'src/assets/images/magicTravel.png',
            desc: 'Многостраничный сайт экскурсий по Саратову и области',
            webLink: 'https://belyaninivan.github.io/MagicTravel', 
            codeLink: 'https://github.com/BelyaninIvan/MagicTravel',
        },
        {
            id: '3',
            name: 'Saratov Tour',
            img: 'src/assets/images/saratovTour.png',
            desc: 'Многостраничный сайт о туристических маршрутах по городу Саратову',
            webLink: 'https://belyaninivan.github.io/SaratovTour', 
            codeLink: 'https://github.com/BelyaninIvan/SaratovTour',
        },
        {
            id: '4',
            name: 'Проект Место',
            img: 'src/assets/images/mesto.png',
            desc: 'Сайт с библиотекой фотографий, который имеет различный функционал',
            webLink: 'https://belyaninivan.github.io/ProjectMesto', 
            codeLink: 'https://github.com/BelyaninIvan/ProjectMesto',
        },
        {
            id: '5',
            name: 'Проект Uber',
            img: 'src/assets/images/uber.png',
            desc: 'Сайт для сервиса такси Uber',
            webLink: 'https://belyaninivan.github.io/bootstrap/', 
            codeLink: 'https://github.com/BelyaninIvan/bootstrap',
        },
      ],
    }
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