<template>
  <section class="info">
    <div class="info__wrapper container flex">
      <div class="info__left">
        <p>Кем вы хотите стать?</p>

        <p>Пора найти себя и выбрать подходящий курс</p>

        <p>Удачи!</p>
        <img src="/src/assets/img/Сова-01 1.svg" alt="" />
      </div>
      <div class="info__right">
        <div class="flex">
          <div class="info__right-personal">
            <img src="/src/assets/img/children.svg" alt="" class="info__image" />
            <div class="info__text">
              <h4>Дети</h4>
              <span>8 - 14 лет</span>
            </div>
          </div>
          <div class="info__right-personal">
            <img src="/src/assets/img/children (1).svg" alt="" class="info__image" />
            <div class="info__text">
              <h4>Подростки</h4>
              <span>14 - 18 лет</span>
            </div>
          </div>
          <div class="info__right-personal">
            <img src="/src/assets/img/family.svg" alt="" class="info__image" />
            <div class="info__text">
              <h4>Взрослые</h4>
              <span>18 — ∞</span>
            </div>
          </div>
        </div>
        <div class="info__right-profession">
          <ul>
            <li><a href="">Робототехника</a></li>
            <li><a href="">Создание игр</a></li>
            <li><a href="">Web-разработка</a></li>
            <li><a href="">Мультимедиа</a></li>
            <li><a href="">Шахматы</a></li>
            <li><a href="">3D-моделирование и дизайн</a></li>
            <li><a href="">Английский язык</a></li>
            <li><a href="">Блогинг</a></li>
            <li><a href="">Soft skills</a></li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>
<style lang="scss">
$primary-color: #f7941d;
$border-radius: 20px;
$font-size: 16px;
$font-weight: 500;
$line-height: 17px;
$img-width: 63px;
$img-height: 70px;

.info {
  margin-top: 40px;

  &__left {
    position: relative;
    border: solid $primary-color;
    border-radius: $border-radius;
    padding: 12px;
    display: inline-block;
    height: 218px;

    p {
      font-size: $font-size;
      font-weight: $font-weight;
      line-height: $line-height;

      &:nth-child(1) {
        font-weight: bold;
      }
    }

    img {
      position: absolute;
      top: 90%;
      left: -20%;
    }
  }

  &__right {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    padding-left: 40px;

    > .flex {
      display: flex;
      justify-content: space-between;
      margin-bottom: 20px;
      position: relative;
      width: 100%;
      border-bottom: 1px solid gray;
    }

    &-personal {
      display: flex;
      align-items: center;
      position: relative;

      &::after {
        content: '';
        position: absolute;
        left: 0;
        right: 0;
        bottom: 0;
        height: 3px;
        z-index: 1;
        transition:
          background-color 0.3s,
          height 0.3s;
      }

      &:hover::after {
        background: $primary-color;
      }

      .info__image {
        margin-right: 20px; /* Отступ между изображением и текстом */
      }

      .info__text {
        display: flex;
        flex-direction: column;
      }

      h4 {
        margin: 0;
      }

      span {
        margin-top: 5px;
      }
    }

    &-profession {
      ul {
        padding: 0;
        list-style: none;
        display: flex;
        flex-wrap: wrap;

        li {
          padding: 10px 20px;
          margin-bottom: 10px;
          margin-right: 20px;
          border-radius: 5px;
          border: red solid 1px;
          font-size: 14px;
          font-weight: $font-weight;
          line-height: $line-height;
          box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);

          a {
            text-decoration: none;
          }
        }
      }
    }
  }
}

@media (max-width: 1300px) {
  .info {
    &__wrapper {
      display: block;
    }
    &__left {
      padding: 12px;
      position: relative;
      height: auto;

      img {
        position: absolute;
        left: 0;
        width: $img-width;
        height: $img-height;
      }

      p {
        font-size: 14px;
        line-height: 20px;
      }
    }
    &__right > .flex {
      padding: 10px;
    }

    &__right-personal {
      padding-top: 80px;
      display: flex;
      flex-direction: column;
    }

    .info__image {
      margin-right: 0;
    }
  }
}
</style>
