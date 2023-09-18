<template>
  <main class="content">
    <h2 class="content__title">Мои проекты</h2>
  </main>
</template>
<script>
export default {
  name: "MainComponent",
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
</style>