<template>
    <header class="header">
        <div class="header__content">
            <h1 class="header__title">Сайт-портфолио</h1>
            <img src="../assets/images/profile.jpg" alt="Фото профиля" class="header__image">
            <div class="header__information">
                <h2 class="header__name">
                    Белянин Иван Романович
                </h2>
                <p class="header__text">
                    Frontend developer
                </p>
                <p class="header__text">
                    22 года, Москва
                </p>
                <p class="header__text">
                    Опыт работы: 2 года верстальщиком; 6 месяцев Frontend developer
                </p>
                <ul class="header__social-list">
                    <li class="header__social-item">
                        <a href="https://hh.ru/resume/5d0b98e5ff08a511c70039ed1f496955546139" class="header__social-link" target="_blank">
                            <img src="../assets/images/min-hh-red.png" alt="Иконка hh" class="header__social-icon">
                        </a>
                    </li>
                    <li class="header__social-item">
                        <a href="https://career.habr.com/belyaninivanr" class="header__social-link" target="_blank">
                            <img src="../assets/images/icons8-habr.svg" alt="Иконка habr" class="header__social-icon">
                        </a>
                    </li>
                    <li class="header__social-item">
                        <a href="https://t.me/BelyaninIvan" class="header__social-link">
                            <img src="../assets/images/free-icon-telegram-2111646.png" alt="Иконка telegram" class="header__social-icon" target="_blank">
                        </a>
                    </li>
                    <li class="header__social-item">
                        <a href="https://www.linkedin.com/in/%D0%B8%D0%B2%D0%B0%D0%BD-%D0%B1%D0%B5%D0%BB%D1%8F%D0%BD%D0%B8%D0%BD-a6a954290/" class="header__social-link" target="_blank">
                            <img src="../assets/images/free-icon-linkedin-3536505.png" alt="Иконка linkedIn" class="header__social-icon">
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>
<script>
export default {
    name: 'HeaderComponent',
}
</script>
<style scoped>
    .header {
        position: relative;
        width: 100%;
        background-color: #223146;
        z-index: 0;
    }

    .header::before {
        content: "";
        background: url('../assets/images/background.jpg') no-repeat;
        background-size: cover;
        position: absolute;
        top: 0px;
        right: 0px;
        bottom: 0px;
        left: 0px;
        opacity: 0.2;
        z-index: -1;
    }

    .header__content {
        max-width: 1280px;
        margin: 0 auto;
        padding: 45px 0;
        display: flex;
        flex-direction: column;
        align-items: center;

        color: #F4F5EF;
    }

    .header__title {
        margin: 0 auto 60px;
        text-align: center;
        color: #F4F5EF;
        font-size: 28px;
        font-weight: 700;
    }

    .header__image {
        width: 200px;
        height: 200px;
        object-fit: cover;
        object-position: top;
        border-radius: 50%;
    }

    .header__information {
        margin-top: 35px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        row-gap: 15px;
    }

    .header_name {
        margin: 0;
        font-size: 28px;
        font-weight: 700;
    }

    .header__text {
        margin: 0;
        max-width: 400px;
        font-size: 20px;
        font-weight: 700;
        text-align: center;
    }

    .header__social-list {
        margin: 0;
        padding: 8px 12px;
        list-style-type: none;
        display: flex;
        align-items: center;
        justify-content: center;
        column-gap: 25px;
    }

    .header__social-icon {
        width: 24px;
        height: 24px;
        object-fit: cover;
    }
</style>