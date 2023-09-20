<template>
  <li class="item">
    <h3 class="item__name">{{ projectsItem.name }}</h3>
    <img :src="projectsItem.img" alt="Превью проекта" class="item__img">
    <p class="item__desc">{{ projectsItem.desc }}</p>
    <MyLinkBtn
      :addr="projectsItem.webLink"
    >
      Посмотреть
    </MyLinkBtn>
    <MyLinkBtn v-show="projectsItem.codeLink != ''"
      :addr="projectsItem.codeLink"
    >
      Изучить код
    </MyLinkBtn>
  </li>
</template>
<script>
export default {
  name: 'ProjectsItem',
  props: {
    projectsItem: {
        type: Object,
    }
  },
}
</script>
<style scoped>
  .item {
    margin: 0;
    padding: 10px 15px;
    min-height: 400px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    row-gap: 15px;
    box-sizing: border-box;
    border-radius: 40px;
    background: #223146;
  }

  .item__name {
    margin: 0;
    color: #F4F5EF;
    font-size: 22px;
    font-weight: 700;
    text-align: center;
  }

  .item__img {
    width: 220px;
    height: 80px;
    border-radius: 10px;
    object-fit: cover;
  }

  .item__desc {
    margin: 0;
    min-height: 120px;
    color: #F4F5EF;
    text-align: center;
    font-size: 20px;
    font-weight: 400;
    display: flex;
    align-items: center;
  }

</style>