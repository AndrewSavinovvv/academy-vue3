<template>
  <section class="info">
    <div class="container flex">
      <div class="info__left">
        <p>Кем вы хотите стать?</p>

        <p>Пора найти себя и выбрать подходящий курс</p>

        <p>Удачи!</p>
        <img src="/src/assets/img/Сова-01 1.svg" alt="" />
      </div>
      <div class="info__right">
        <div class="flex">
          <div class="info__right-perlonal">
            <div class="flex">
              <img src="/src/assets/img/children.svg" alt="" />
              <h4>Дети</h4>
            </div>
            <span>8 - 14 лет</span>
          </div>
          <div class="info__right-perlonal">
            <div class="flex">
              <img src="/src/assets/img/children (1).svg" alt="" />
              <h4>Подростки</h4>
            </div>
            <span>14 - 18 лет</span>
          </div>
          <div class="info__right-perlonal">
            <div class="flex">
              <img src="/src/assets/img/family.svg" alt="" />
              <h4>Взрослые</h4>
            </div>
            <span>18 — ∞ </span>
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

    &-perlonal {
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

      .flex {
        display: flex;
        align-items: center;
      }

      img {
        margin-right: 10px;
      }

      h4 {
        margin: 0;
      }

      span {
        margin-left: 10px;
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

@media (max-width: 1198px) {
  .info {
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

    &__right-perlonal {
      padding-top: 80px;
    }
  }
}
</style>
