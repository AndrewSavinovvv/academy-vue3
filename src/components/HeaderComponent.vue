<template>
  <header class="header">
    <div class="container flex space-between">
      <img class="header__logo" src="/src/assets/img/logo.svg" alt="Academy Logo" />
      <div class="header__burger-menu" @click="toggleMenu()">
        <div class="header__burger-bar"></div>
        <div class="header__burger-bar"></div>
        <div class="header__burger-bar"></div>
      </div>
      <ul class="header__list">
        <li><img src="/src/assets/img/все.svg" alt="" /> Все курсы</li>
        <li>Мероприятия</li>
        <li>Базы знаний</li>
        <li>Карьера</li>
        <li>
          <a href="#">
            <img src="/src/assets/img/geo.svg" alt="" />Нижний Новгород
            <img src="/src/assets/img/down.svg" alt="" />
          </a>
        </li>
        <li>8 800 950 33 98</li>
        <li>
          <button class="header__btn"><img src="/src/assets/img/вход.svg" alt="" />Войти</button>
        </li>
      </ul>
    </div>
  </header>
</template>

<script setup>
function toggleMenu() {
  const menu = document.querySelector('.header__list')
  menu.classList.toggle('active')
}
</script>

<style lang="scss">
html,
body {
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}

.header {
  padding: 20px;
  position: relative;

  &__logo {
    width: 100px;
    height: 70px;
  }

  &__list {
    display: flex;
    align-items: center;
    list-style: none;
    color: #000000;
    max-width: 100%;

    &:nth-child(5) {
      padding-left: 40px;
    }

    li {
      margin-left: 20px;
    }

    a {
      color: #000000;
      font-weight: 500;
      display: flex;
      align-items: center;
      font-size: 14px;

      img {
        margin-right: 8px;
      }
    }
  }

  &__btn {
    color: black;
    background-color: white;
    border: none;
    cursor: pointer;
    display: flex;
    align-items: center;

    img {
      margin-right: 8px;
    }
  }

  &__burger-menu {
    display: none;
    flex-direction: column;
    cursor: pointer;

    .header__burger-bar {
      width: 25px;
      height: 3px;
      background-color: black;
      margin: 3px 0;

      &:nth-child(2) {
        width: 20px;
        margin-left: 5px;
      }
    }
  }
}

@media (max-width: 1198px) {
  .header__list {
    display: none;
    flex-direction: column;
    position: absolute;
    top: 85%;
    left: 0px;
    z-index: 999;
    background-color: white;
    width: 100%;
    box-sizing: border-box;

    &:nth-child(5) {
      padding-left: 0;
    }

    &.active {
      display: flex;
      align-items: flex-start;
    }

    li {
      margin: 10px 0;
      text-align: left;
    }
  }

  .header__burger-menu {
    display: flex;
    justify-content: center;
  }

  .header__container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
</style>
