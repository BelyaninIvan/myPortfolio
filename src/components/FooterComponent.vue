<template>
  <footer class="footer">
    <h2 class="footer__title">2023 год. Белянин Иван Романович</h2>
    <p class="footer__desc">
      Сайт разработан в качестве портфолио Frontend разработчика Белянина Ивана Романовича. Данный сайт предназначен для демонстрации проектов работодателям.
    </p>
  </footer>
</template>
<script>
export default {
  name: 'FooterComponent',
}
</script>
<style scoped>
  .footer {
    margin: 0 auto;
    padding: 25px 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    row-gap: 25px;
    color: rgba(244, 245, 239, 0.7);
    background: #223146;
  }

  .footer__title {
    margin: 0;
    text-align: center;
    font-size: 22px;
    font-weight: 700;
  }

  .footer__desc {
    margin: 0 auto;
    max-width: 900px;
    text-align: center;
    font-size: 18px;
    font-weight: 400;
  }
</style>